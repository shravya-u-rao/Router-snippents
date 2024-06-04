js
npx create-react-app my-app --template typescript
npx create-react-app --template typescript .
npm i react-bootstrap
npm install -g sass
npm i socket.io-client

-----
Plugins
Auto rename Tag
Bracket Pair Color
ES7 react/red.. snippet
Highlight Matching
Live server
Matrerial Icon Theme
One Dark theme Pro
Simple React Client


js
Routing

npm install -S react-router-dom
npm i -D react-router-dom@latest
import { BrowserRouter, Routes, Route } from "react-router-dom";

 <BrowserRouter>
      <Routes>
        <Route path="/" Component={HomeScreen} />
        <Route path="/detail" Component={DetailsScreen} />
        <Route
          path="/profile/:firstname/:secondname"
          Component={ProfileScreen}
        />
      </Routes>
    </BrowserRouter>
    
----------------------------------------------------
HomeScreen
import { useNavigate } from "react-router-dom";

let navigate = useNavigate();

navigate(`/detail?item_id=${i}`);

navigate("/profile/Abhijth/Mogaveera");

--------------------------------------------------
DetailsScreen
import { useSearchParams } from "react-router-dom";
const [searchParams] = useSearchParams();

  return (
    <div>
      <h1>{`ID = ${searchParams.get("item_id")}`}</h1>
    </div>
  );
-----------------------------------------------------
ProfileScreen
import { useParams } from "react-router-dom";

const { firstname, secondname } = useParams<{
        firstname: string;
        secondname: string;
 }>();
--------------------------------------------------
navigate(-1);
