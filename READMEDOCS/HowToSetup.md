First setup backend environment, commands in order are:

python -m venv venv

source venv/bin/activate

pip install --upgrade pip

pip install -r requirements.txt

uvicorn app:app --host 0.0.0.0 --port 3000

Backend is now running on port 3000.



To run frontend, commands in order are:

cd frontend

npm install

npm run dev

Frontend is now running on port 5173.



Login for the chatbot is:

email: wicked@gmail.com
password: windows6355
