## Custom Pagination Component

In this project directory, we are having a sample for custom pagination component.

1. Simple and light weight.
1. Customaizable and Reusable.
1. Responsive.
1. No-need of dependency packages (except react and react-dom)

```javascript
import Pagination from "custom-react-pagination";

const App = () => {
  const [currentPage, setCurrentPage] = useState(1); // initial page number to start.
  const [userPerPage, setUserPerPage] = useState(10); // initial number of users per page to start.
  return (
    <Pagination
      // current/initial page number, which can be changed
      page={currentPage}
      // dispatcher to set the current page number
      onPageChange={setCurrentPage}
      // initial no.of users to be rendered per page
      itemsPerPage={userPerPage}
      // dispatcher to set the no.of users per page
      setItemsPerPage={setUserPerPage}
      // below are optional properties

      totalItems={500} // for total number of items (default to 50 items)
      pageNumberLimit={10} // for number of pageNumbers in the page controller (default to 5 page numbers)
      boderColor="#000000" // for custom border color of pagination (default color "#fff" which is white color)
      labelColor="#000000" // for custom label on button color (default color "#fff" which is white color)
      prevBtnLabel="Prev" // for custom label on button (default label "Prev")
      nextBtnLabel="Next" // for custom label on button (default label "Next")
      moreBtnLabel="&hellip;" // for custom label on more button (default label "&hellip;" which is "..." )
      itemsInputLabel="Items Per Page" // for custom label on itemsNumber input field (default label "Items Per Page")
    />
  );
};

export default App;
```

In the above sample, the currentpage and userPerPage has to be managed in parent component. Like below,

```javascript
const [currentPage, setCurrentPage] = useState(1); // initial page number to start.
const [userPerPage, setUserPerPage] = useState(10); // initial number of users per page to start.
```

Here is the sample customaized pagination component.

![Sample Image](/sample-pagination.png)

## Available Scripts

In the project directory, you can simply clone it and run by:

### `npm install`

Install's the package dependencies and devDependencies.

You can npm install any other packages and update them.

### `npm run build`

Remove the old build folder and running the script will build new build folder as per the update made.
