<body>
  <div class="card">
      <div class="header">
        <div class="image">
          <svg
            fill="none"
            viewBox="0 0 24 24"
            stroke-width="1.5"
            stroke="currentColor"
            aria-hidden="true"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              d="M12 9v3.75m-9.303 3.376c-.866 1.5.217 3.374 1.948 3.374h14.71c1.73 0 2.813-1.874 1.948-3.374L13.949 3.378c-.866-1.5-3.032-1.5-3.898 0L2.697 16.126zM12 15.75h.007v.008H12v-.008z"
            ></path>
          </svg>
        </div>
        <div class="content">
          <span class="title">Quest Not Found</span>
          <p class="message">
            The quest you are looking for could not be found. Please ensure you have the correct link and try again.
          </p>
        </div>
        <div class="actions">
          <button onclick="location.replace('/customizable-quests/')" type="button" class="desactivate">Back to LearnQuest Custom</button>
          <button onclick="location.replace('/')" type="button" class="cancel">Back to Home Page</button>
        </div>
      </div>
    </div>
    <style>
  @import url('https://fonts.googleapis.com/css2?family=Inter:ital,opsz,wght@0,14..32,100..900;1,14..32,100..900&display=swap');
      .card {
    overflow: hidden;
    position: relative;
    background-color: #ffffff;
    text-align: left;
    border-radius: 0.5rem;
    max-width: 320px;
    box-shadow:
      0 20px 25px -5px rgba(0, 0, 0, 0.1),
      0 10px 10px -5px rgba(0, 0, 0, 0.04);
  font-family: 'Inter';
  }
  
  .header {
    padding: 1.25rem 1rem 1rem 1rem;
    background-color: #ffffff;
  }
  
  .image {
    display: flex;
    margin-left: auto;
    margin-right: auto;
    background-color: #fee2e2;
    flex-shrink: 0;
    justify-content: center;
    align-items: center;
    width: 3rem;
    height: 3rem;
    border-radius: 9999px;
  }
  
  body {
          display: flex;
          justify-content: center;
          align-items: center;
          min-height: 100vh;
          margin: 0;
          background-color: #f0f0f0;
      }
  
  .image svg {
    color: #dc2626;
    width: 1.5rem;
    height: 1.5rem;
  }
  
  .content {
    margin-top: 0.75rem;
    text-align: center;
  }
  
  .title {
    color: #111827;
    font-size: 1rem;
    font-weight: 600;
    line-height: 1.5rem;
  }
  
  .message {
    margin-top: 0.5rem;
    color: #6b7280;
    font-size: 0.875rem;
    line-height: 1.25rem;
  }
  
  .actions {
    margin: 0.75rem 1rem;
    background-color: #f9fafb;
  }
  
  .desactivate {
    display: inline-flex;
    padding: 0.5rem 1rem;
    background-color: #dc2626;
    color: #ffffff;
    font-size: 1rem;
    line-height: 1.5rem;
    font-weight: 500;
    justify-content: center;
    width: 100%;
    border-radius: 0.375rem;
    border-width: 1px;
    border-color: transparent;
    box-shadow: 0 1px 2px 0 rgba(0, 0, 0, 0.05);
    transition: background-color 0.3s ease, transform 0.2s ease-in-out;
  }
  
  .desactivate:hover {
    background-color: #b91c1c;
    transform: translateY(-3px);
  }
  
  .cancel {
    display: inline-flex;
    margin-top: 0.75rem;
    padding: 0.5rem 1rem;
    background-color: #ffffff;
    color: #374151;
    font-size: 1rem;
    line-height: 1.5rem;
    font-weight: 500;
    justify-content: center;
    width: 100%;
    border-radius: 0.375rem;
    border: 1px solid #d1d5db;
    box-shadow: 0 1px 2px 0 rgba(0, 0, 0, 0.05);
    transition: background-color 0.3s ease, transform 0.2s ease-in-out;
  }
  
  .cancel:hover {
    background-color: #f3f4f6;
    transform: translateY(-3px);
  }
  
    </style>
    </body>