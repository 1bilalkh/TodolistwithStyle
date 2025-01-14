import React, { useState } from "react";

function Todolist() {
  const [name, setName] = useState("");

  let [todolist, Settodolist] = useState([]);

  const saveList = (e) => {
    let toname = e.target.toname.value;
    if (!todolist.includes(toname)) {
      let finalTdodo = [...todolist, toname];
      Settodolist(finalTdodo);
    } else {
      alert("to do name already exit");
    }

    e.preventDefault();
  };

  let list = todolist.map((value, index) => {
    return (
      <>
        <TodoListShowing
          value={value}
          key={index}
          indexNumber={index}
          todolist={todolist}
          Settodolist={Settodolist}
        />
      </>
    );
  });

  return (
    <>
      <h1 className="countheading">Get Things Done!</h1>
      <div className="counterapp maintodolist">
        <div className="todolist">
          <form onSubmit={saveList}>
            <div className="field_btn">
              <input type="text" name="toname" placeholder="Whats Happening" />
              <button>
                <svg
                  fill="#000000"
                  height="16px"
                  width="16px"
                  version="1.1"
                  id="Layer_1"
                  xmlns="http://www.w3.org/2000/svg"
                  xmlns:xlink="http://www.w3.org/1999/xlink"
                  viewBox="0 0 455 455"
                >
                  <polygon
                    points="455,212.5 242.5,212.5 242.5,0 212.5,0 212.5,212.5 0,212.5 0,242.5 212.5,242.5 212.5,455 242.5,455 242.5,242.5 
                                    455,242.5 "
                  />
                </svg>
              </button>
            </div>
          </form>
          <div className="outerdiv">{list}</div>
        </div>
      </div>
    </>
  );
}

function TodoListShowing({ value, indexNumber, todolist, Settodolist }) {
  let [status, setStatus] = useState(false);
  let Dterow = () => {
    let finalTdodo = todolist.filter((v, i) => i != indexNumber);
    Settodolist(finalTdodo);
  };
  let lineadd = () => {
    setStatus(!status);
  };

  return (
    <>
      <li onClick={lineadd} className={status ? "minus" : ""}>
        <span className="backgroundli"></span>
        <span className="numberstyle">{indexNumber + 1}</span>
        <span className="valuelist">{value}</span>
        <span onClick={Dterow}>
          <svg
            fill="#000000"
            version="1.1"
            id="Capa_1"
            xmlns="http://www.w3.org/2000/svg"
            width="16px"
            height="16px"
            viewBox="0 0 83 83"
          >
            <g>
              <path
                d="M81,36.166H2c-1.104,0-2,0.896-2,2v6.668c0,1.104,0.896,2,2,2h79c1.104,0,2-0.896,2-2v-6.668
                        C83,37.062,82.104,36.166,81,36.166z"
              />
            </g>
          </svg>
        </span>
      </li>
    </>
  );
}

export default Todolist;

