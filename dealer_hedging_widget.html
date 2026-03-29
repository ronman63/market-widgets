<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dealer Hedging Dynamics - Interactive Widget</title>
    <script crossorigin src="https://unpkg.com/react@18/umd/react.production.min.js"></script>
    <script crossorigin src="https://unpkg.com/react-dom@18/umd/react-dom.production.min.js"></script>
    <script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>
    <style>
        body {
            margin: 0;
            padding: 0;
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
        }
    </style>
</head>
<body>
    <div id="root"></div>
    
    <script type="text/babel">
        const { useState } = React;

        function DealerHedgingWidget() {
          const [spxPrice, setSpxPrice] = useState(6400);
          const [postExpiration, setPostExpiration] = useState(false);
          
          const strikePrice = 6475;
          const minPrice = 5900;
          const maxPrice = 7000;
          
          const calculateDealerAction = () => {
            if (postExpiration) {
              return { action: "NO HEDGING", intensity: 0, color: "#64748b" };
            }
            
            const distance = spxPrice - strikePrice;
            const normalizedDistance = Math.abs(distance) / 300;
            
            if (distance > 0) {
              return { 
                action: "BUYING FUTURES", 
                intensity: Math.min(normalizedDistance, 1),
                color: "#10b981",
                description: "Dealers buy S&P futures to hedge short calls → Creates resistance"
              };
            } else {
              return { 
                action: "SELLING FUTURES", 
                intensity: Math.min(normalizedDistance, 1),
                color: "#ef4444",
                description: "Dealers sell S&P futures as delta decreases → Removes support"
              };
            }
          };
          
          const dealerAction = calculateDealerAction();
          
          const priceToPercent = (price) => {
            return ((price - minPrice) / (maxPrice - minPrice)) * 100;
          };
          
          const currentPercent = priceToPercent(spxPrice);
          const strikePercent = priceToPercent(strikePrice);
          
          return (
            <div style={{
              minHeight: '100vh',
              background: 'linear-gradient(135deg, #0f172a 0%, #1e293b 100%)',
              padding: '48px 24px',
              fontFamily: '-apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif',
              color: '#f1f5f9'
            }}>
              <div style={{
                maxWidth: '900px',
                margin: '0 auto'
              }}>
                {/* Header */}
                <div style={{ marginBottom: '48px', textAlign: 'center' }}>
                  <h1 style={{
                    fontSize: '32px',
                    fontWeight: '700',
                    marginBottom: '12px',
                    letterSpacing: '-0.02em',
                    background: 'linear-gradient(135deg, #60a5fa 0%, #3b82f6 100%)',
                    WebkitBackgroundClip: 'text',
                    WebkitTextFillColor: 'transparent',
                    backgroundClip: 'text'
                  }}>
                    Dealer Hedging Dynamics
                  </h1>
                  <p style={{
                    fontSize: '16px',
                    color: '#94a3b8',
                    maxWidth: '600px',
                    margin: '0 auto',
                    lineHeight: '1.6'
                  }}>
                    Move the slider to see how JPMorgan's options position creates artificial market support through dealer hedging
                  </p>
                </div>

                {/* Toggle */}
                <div style={{
                  display: 'flex',
                  justifyContent: 'center',
                  marginBottom: '40px',
                  gap: '8px'
                }}>
                  <button
                    onClick={() => setPostExpiration(false)}
                    style={{
                      padding: '12px 24px',
                      fontSize: '14px',
                      fontWeight: '600',
                      border: 'none',
                      borderRadius: '8px',
                      cursor: 'pointer',
                      transition: 'all 0.2s',
                      background: !postExpiration ? '#3b82f6' : '#1e293b',
                      color: !postExpiration ? '#ffffff' : '#64748b',
                      border: !postExpiration ? 'none' : '1px solid #334155'
                    }}>
                    Before March 31
                  </button>
                  <button
                    onClick={() => setPostExpiration(true)}
                    style={{
                      padding: '12px 24px',
                      fontSize: '14px',
                      fontWeight: '600',
                      border: 'none',
                      borderRadius: '8px',
                      cursor: 'pointer',
                      transition: 'all 0.2s',
                      background: postExpiration ? '#ef4444' : '#1e293b',
                      color: postExpiration ? '#ffffff' : '#64748b',
                      border: postExpiration ? 'none' : '1px solid #334155'
                    }}>
                    After March 31 🚪
                  </button>
                </div>

                {/* Main Visualization */}
                <div style={{
                  background: '#1e293b',
                  borderRadius: '16px',
                  padding: '40px',
                  border: '1px solid #334155',
                  marginBottom: '32px'
                }}>
                  {/* Current Price Display */}
                  <div style={{
                    textAlign: 'center',
                    marginBottom: '40px'
                  }}>
                    <div style={{
                      fontSize: '14px',
                      color: '#94a3b8',
                      marginBottom: '8px',
                      fontWeight: '500',
                      letterSpacing: '0.05em',
                      textTransform: 'uppercase'
                    }}>
                      S&P 500 Current Price
                    </div>
                    <div style={{
                      fontSize: '56px',
                      fontWeight: '700',
                      fontFamily: '"Courier New", monospace',
                      color: spxPrice > strikePrice ? '#10b981' : '#ef4444',
                      transition: 'color 0.3s'
                    }}>
                      {spxPrice.toLocaleString()}
                    </div>
                    <div style={{
                      fontSize: '14px',
                      color: '#64748b',
                      marginTop: '4px'
                    }}>
                      {spxPrice > strikePrice ? `+${(spxPrice - strikePrice)} above` : `${(spxPrice - strikePrice)} below`} strike ({strikePrice})
                    </div>
                  </div>

                  {/* Price Slider */}
                  <div style={{ marginBottom: '48px' }}>
                    <div style={{
                      position: 'relative',
                      height: '80px',
                      marginBottom: '16px'
                    }}>
                      {/* Strike price line */}
                      <div style={{
                        position: 'absolute',
                        left: `${strikePercent}%`,
                        top: '0',
                        bottom: '0',
                        width: '2px',
                        background: '#3b82f6',
                        zIndex: 1
                      }}>
                        <div style={{
                          position: 'absolute',
                          top: '-30px',
                          left: '50%',
                          transform: 'translateX(-50%)',
                          fontSize: '12px',
                          color: '#3b82f6',
                          fontWeight: '600',
                          whiteSpace: 'nowrap'
                        }}>
                          ⚡ Strike: 6,475
                        </div>
                      </div>

                      {/* Slider track */}
                      <div style={{
                        position: 'absolute',
                        top: '50%',
                        left: '0',
                        right: '0',
                        height: '8px',
                        background: '#0f172a',
                        borderRadius: '4px',
                        transform: 'translateY(-50%)'
                      }}>
                        <div style={{
                          position: 'absolute',
                          left: '0',
                          top: '0',
                          bottom: '0',
                          width: `${currentPercent}%`,
                          background: `linear-gradient(90deg, ${spxPrice > strikePrice ? '#10b981' : '#ef4444'}, ${spxPrice > strikePrice ? '#34d399' : '#f87171'})`,
                          borderRadius: '4px',
                          transition: 'all 0.2s'
                        }} />
                      </div>

                      {/* Slider input */}
                      <input
                        type="range"
                        min={minPrice}
                        max={maxPrice}
                        step={25}
                        value={spxPrice}
                        onChange={(e) => setSpxPrice(Number(e.target.value))}
                        style={{
                          position: 'absolute',
                          top: '50%',
                          left: '0',
                          right: '0',
                          width: '100%',
                          transform: 'translateY(-50%)',
                          opacity: 0,
                          cursor: 'pointer',
                          zIndex: 2,
                          height: '40px'
                        }}
                      />
                      <div style={{
                        position: 'absolute',
                        left: `${currentPercent}%`,
                        top: '50%',
                        width: '24px',
                        height: '24px',
                        background: '#ffffff',
                        border: `3px solid ${spxPrice > strikePrice ? '#10b981' : '#ef4444'}`,
                        borderRadius: '50%',
                        transform: 'translate(-50%, -50%)',
                        boxShadow: '0 4px 12px rgba(0, 0, 0, 0.4)',
                        transition: 'border-color 0.2s',
                        zIndex: 3
                      }} />
                    </div>

                    {/* Price labels */}
                    <div style={{
                      display: 'flex',
                      justifyContent: 'space-between',
                      fontSize: '12px',
                      color: '#64748b',
                      fontFamily: '"Courier New", monospace'
                    }}>
                      <span>5,900</span>
                      <span>6,200</span>
                      <span>6,500</span>
                      <span>6,800</span>
                      <span>7,000</span>
                    </div>
                  </div>

                  {/* Dealer Action Display */}
                  <div style={{
                    background: postExpiration ? '#0f172a' : (spxPrice > strikePrice ? 'rgba(16, 185, 129, 0.1)' : 'rgba(239, 68, 68, 0.1)'),
                    border: `2px solid ${postExpiration ? '#334155' : dealerAction.color}`,
                    borderRadius: '12px',
                    padding: '32px',
                    textAlign: 'center',
                    transition: 'all 0.3s'
                  }}>
                    <div style={{
                      fontSize: '14px',
                      color: '#94a3b8',
                      marginBottom: '12px',
                      fontWeight: '500',
                      letterSpacing: '0.05em',
                      textTransform: 'uppercase'
                    }}>
                      Dealer Action
                    </div>
                    <div style={{
                      fontSize: '28px',
                      fontWeight: '700',
                      color: dealerAction.color,
                      marginBottom: '16px',
                      transition: 'color 0.3s',
                      letterSpacing: '0.02em'
                    }}>
                      {dealerAction.action}
                    </div>
                    
                    {!postExpiration && (
                      <>
                        <div style={{
                          fontSize: '14px',
                          color: '#cbd5e1',
                          marginBottom: '20px',
                          lineHeight: '1.6'
                        }}>
                          {dealerAction.description}
                        </div>
                        
                        <div style={{
                          height: '8px',
                          background: '#0f172a',
                          borderRadius: '4px',
                          overflow: 'hidden'
                        }}>
                          <div style={{
                            height: '100%',
                            width: `${dealerAction.intensity * 100}%`,
                            background: dealerAction.color,
                            transition: 'all 0.3s',
                            borderRadius: '4px'
                          }} />
                        </div>
                        <div style={{
                          fontSize: '12px',
                          color: '#64748b',
                          marginTop: '8px'
                        }}>
                          Hedging Intensity: {Math.round(dealerAction.intensity * 100)}%
                        </div>
                      </>
                    )}
                    
                    {postExpiration && (
                      <div style={{
                        fontSize: '16px',
                        color: '#94a3b8',
                        lineHeight: '1.6',
                        fontStyle: 'italic'
                      }}>
                        Options expired. Dealers no longer hedging.<br/>
                        Market trades on fundamentals only.
                      </div>
                    )}
                  </div>
                </div>

                {/* Explainer Cards */}
                <div style={{
                  display: 'grid',
                  gridTemplateColumns: 'repeat(auto-fit, minmax(280px, 1fr))',
                  gap: '16px',
                  marginBottom: '32px'
                }}>
                  <div style={{
                    background: '#1e293b',
                    border: '1px solid #334155',
                    borderRadius: '12px',
                    padding: '24px'
                  }}>
                    <div style={{
                      fontSize: '18px',
                      fontWeight: '600',
                      marginBottom: '12px',
                      color: '#10b981'
                    }}>
                      ▲ Above Strike
                    </div>
                    <div style={{
                      fontSize: '14px',
                      color: '#cbd5e1',
                      lineHeight: '1.6'
                    }}>
                      Dealers buy S&P futures to hedge their short call position. This creates <strong>artificial resistance</strong> — mechanical selling pressure caps rallies.
                    </div>
                  </div>

                  <div style={{
                    background: '#1e293b',
                    border: '1px solid #334155',
                    borderRadius: '12px',
                    padding: '24px'
                  }}>
                    <div style={{
                      fontSize: '18px',
                      fontWeight: '600',
                      marginBottom: '12px',
                      color: '#ef4444'
                    }}>
                      ▼ Below Strike
                    </div>
                    <div style={{
                      fontSize: '14px',
                      color: '#cbd5e1',
                      lineHeight: '1.6'
                    }}>
                      Dealers sell S&P futures as their hedge requirement decreases. This removes <strong>artificial support</strong> — no mechanical buying to catch falls.
                    </div>
                  </div>

                  <div style={{
                    background: '#1e293b',
                    border: '1px solid #334155',
                    borderRadius: '12px',
                    padding: '24px'
                  }}>
                    <div style={{
                      fontSize: '18px',
                      fontWeight: '600',
                      marginBottom: '12px',
                      color: '#64748b'
                    }}>
                      🚪 Post-Expiration
                    </div>
                    <div style={{
                      fontSize: '14px',
                      color: '#cbd5e1',
                      lineHeight: '1.6'
                    }}>
                      After March 31, the options expire and dealer hedging vanishes. Market trades on fundamentals with <strong>no artificial floor or ceiling</strong>.
                    </div>
                  </div>
                </div>

                {/* Bottom Explainer */}
                <div style={{
                  background: 'linear-gradient(135deg, rgba(59, 130, 246, 0.1) 0%, rgba(16, 185, 129, 0.1) 100%)',
                  border: '1px solid rgba(59, 130, 246, 0.3)',
                  borderRadius: '12px',
                  padding: '32px',
                  fontSize: '14px',
                  color: '#cbd5e1',
                  lineHeight: '1.8'
                }}>
                  <div style={{
                    fontSize: '18px',
                    fontWeight: '600',
                    marginBottom: '16px',
                    color: '#60a5fa'
                  }}>
                    🎯 The Key Insight
                  </div>
                  <p style={{ margin: '0 0 12px 0' }}>
                    JPMorgan's Hedged Equity Fund sells massive call options on the S&P 500. The dealers who buy these calls must hedge by buying/selling futures, which creates artificial price stability around the strike price (6,475).
                  </p>
                  <p style={{ margin: '0 0 12px 0' }}>
                    <strong>The "trap door":</strong> When options expire March 31 with the S&P below the strike, dealer hedging disappears. The market loses its mechanical support — leaving only fundamental buyers to catch any fall.
                  </p>
                  <p style={{ margin: '0' }}>
                    <strong>What to watch:</strong> If the S&P closes March 31 below 6,475, April trading begins without the dealer bid that has been cushioning declines all quarter.
                  </p>
                </div>
              </div>
            </div>
          );
        }

        ReactDOM.render(<DealerHedgingWidget />, document.getElementById('root'));
    </script>
</body>
</html>
