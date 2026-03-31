# AI-WAF
1. Install and move to AI-WAF directory
  ```
  git clone https://github.com/PhongNoCode/AI-WAF.git
  cd AI-WAF
  ```
2. Create a virtual environment and models folder
  ```
  python3 -m venv venv
  source venv/bin/activate
  mkdir models
  ```
3. Install all libraries
  ```
  pip install -r requirements.txt
  ```
4. Filter the dataset
  ```
  python3 filter_data.py
  ```
5. Add more malware payloads to the dataset
  ```
  python3 add_payloads.py
  ```
6. Run file ai_service to activate AI WAF
  ```
  uvicorn ai_service:app --port 8000
  ```
7. Open another terminal to run web
  ```
  python3 web_app.py
  ```
8. Test these payloads and compare to modsecurity
  ```
  11' or  WEIGHT_STRING(@@version)=WEIGHT_STRING(@@version) --
  1+un/**/ion+se/**/lect+1,2,3--
  ```
