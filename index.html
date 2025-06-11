<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <title>kalkulator_047</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet" />
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@600&display=swap" rel="stylesheet" />
    <link rel="stylesheet" href="style.css">
</head>

<body>

    <main class="container" role="main" aria-label="Calculator application">
        <div class="card" role="region" aria-label="Calculator">
            <div id="display" aria-live="polite" aria-atomic="true" aria-label="Calculator display">0</div>
            <div class="row g-3">
                <div class="col-3"><button class="btn btn-calc" data-key="7" aria-label="Digit 7"
                        type="button">7</button></div>
                <div class="col-3"><button class="btn btn-calc" data-key="8" aria-label="Digit 8"
                        type="button">8</button></div>
                <div class="col-3"><button class="btn btn-calc" data-key="9" aria-label="Digit 9"
                        type="button">9</button></div>
                <div class="col-3"><button class="btn btn-calc btn-operator" data-key="/" aria-label="Divide"
                        type="button">÷</button></div>

                <div class="col-3"><button class="btn btn-calc" data-key="4" aria-label="Digit 4"
                        type="button">4</button></div>
                <div class="col-3"><button class="btn btn-calc" data-key="5" aria-label="Digit 5"
                        type="button">5</button></div>
                <div class="col-3"><button class="btn btn-calc" data-key="6" aria-label="Digit 6"
                        type="button">6</button></div>
                <div class="col-3"><button class="btn btn-calc btn-operator" data-key="*" aria-label="Multiply"
                        type="button">×</button></div>

                <div class="col-3"><button class="btn btn-calc" data-key="1" aria-label="Digit 1"
                        type="button">1</button></div>
                <div class="col-3"><button class="btn btn-calc" data-key="2" aria-label="Digit 2"
                        type="button">2</button></div>
                <div class="col-3"><button class="btn btn-calc" data-key="3" aria-label="Digit 3"
                        type="button">3</button></div>
                <div class="col-3"><button class="btn btn-calc btn-operator" data-key="-" aria-label="Subtract"
                        type="button">−</button></div>

                <div class="col-3"><button class="btn btn-calc" data-key="0" aria-label="Digit 0"
                        type="button">0</button></div>
                <div class="col-3"><button class="btn btn-calc" data-key="." aria-label="Decimal point"
                        type="button">.</button></div>
                <div class="col-3"><button class="btn btn-calc btn-clear" data-key="clear" aria-label="Clear input"
                        type="button">C</button></div>
                <div class="col-3"><button class="btn btn-calc btn-operator" data-key="+" aria-label="Add"
                        type="button">+</button></div>

                <div class="col-6"><button class="btn btn-calc btn-equal" data-key="="
                        aria-label="Calculate result" type="button">=</button></div>
            </div>
            <div id="message" role="alert" aria-live="assertive" class="error-message visually-hidden"></div>
        </div>
    </main>

    <script>
        (() => {
            const display = document.getElementById('display');
            const message = document.getElementById('message');
            const buttons = document.querySelectorAll('.btn-calc');
            let input = '';
            let resetDisplay = false;

            const updateDisplay = () => {
                display.textContent = input || '0';
            };

            const clearInput = () => {
                input = '';
                updateDisplay();
                clearMessage();
            };

            const clearMessage = () => {
                message.textContent = '';
                message.classList.add('visually-hidden');
            };

            const showMessage = (text) => {
                message.textContent = text;
                message.classList.remove('visually-hidden');
            };

            const appendToInput = (char) => {
                if (resetDisplay) {
                    input = '';
                    resetDisplay = false;
                }
                if (char === '.') {
                    const segments = input.split(/[\+\-\*\/]/);
                    if (segments[segments.length - 1].includes('.')) return;
                }
                input += char;
                updateDisplay();
            };

            const safeEval = (expr) => {
                if (/[^0-9+\-*/%.() ]/.test(expr)) {
                    throw new Error('Invalid characters detected.');
                }
                let balance = 0;
                for (const char of expr) {
                    if (char === '(') balance++;
                    else if (char === ')') balance--;
                    if (balance < 0) throw new Error('Unbalanced parentheses.');
                }
                if (balance !== 0) throw new Error('Unbalanced parentheses.');

                expr = expr.replace(/(\d+\.?\d*)%/g, '($1/100)');

                try {
                    return Function('"use strict";return (' + expr + ')')();
                } catch {
                    throw new Error('Invalid mathematical expression.');
                }
            };

            const calculate = () => {
                try {
                    clearMessage();
                    if (!input.trim()) {
                        showMessage('Please enter an expression.');
                        return;
                    }
                    const result = safeEval(input);
                    if (typeof result === 'number' && Number.isFinite(result)) {
                        input = result.toString();
                        updateDisplay();
                        resetDisplay = true;
                    } else {
                        throw new Error('Calculation resulted in invalid value.');
                    }
                } catch (e) {
                    showMessage(e.message);
                }
            };

            buttons.forEach(btn => {
                btn.addEventListener('click', () => {
                    const key = btn.dataset.key;
                    clearMessage();
                    switch (key) {
                        case 'clear':
                            clearInput();
                            break;
                        case '=':
                            calculate();
                            break;
                        default:
                            appendToInput(key);
                            break;
                    }
                });
            });

            window.addEventListener('keydown', (e) => {
                clearMessage();
                if (e.target.tagName === 'INPUT' || e.target.tagName === 'TEXTAREA') return;

                if (e.key >= '0' && e.key <= '9') {
                    appendToInput(e.key);
                } else if (['+', '-', '*', '/'].includes(e.key)) {
                    appendToInput(e.key);
                } else if (e.key === '.') {
                    appendToInput(e.key);
                } else if (e.key === 'Enter' || e.key === '=') {
                    e.preventDefault();
                    calculate();
                } else if (e.key === 'Backspace') {
                    input = input.slice(0, -1);
                    updateDisplay();
                } else if (e.key === 'Escape') {
                    clearInput();
                }
            });

            updateDisplay();
        })();
    </script>
</body>

</html>
