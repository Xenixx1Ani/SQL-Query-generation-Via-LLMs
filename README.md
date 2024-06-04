# SQL Query Generator

This project generates SQL queries from natural language input using a pre-trained T5 model. The T5 model is used for converting natural language questions into corresponding SQL queries. This can be particularly useful for automating query generation for databases.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/SQLQueryGenerator.git
   ```
2. Navigate to the project directory:
   ```bash
   cd SQLQueryGenerator
   ```

## Usage

Run the notebook to generate SQL queries.



You will be prompted to enter a query in natural language, and the script will output the corresponding SQL query.

### Example

```
Enter Query: List the names of all ships.
Output: SELECT ship_name FROM ship_data;
```

### Models

The project supports using a local model or fetching a model from Hugging Face. By default, it uses a model stored locally. You can update the `model_path` in `main.py` to fetch a model from Hugging Face instead.

#### Using a Local Model

1. Download or place your model in the `./model/t5-small-text-to-sql/` directory.
2. Ensure `model_path` in `main.py` points to this local directory.

#### Using a Hugging Face Model

To use a model from Hugging Face, update `model_path` in `main.py` to the appropriate model name. For example:

```
model_path = "cssupport/t5-small-awesome-text-to-sql"
```


## Credits

This project uses the [T5 model](https://huggingface.co/t5-small) for natural language processing. Special thanks to the Hugging Face team for providing the models and the `transformers` library. The pretrained model used in the noteboob was sourced form [cssupport/t5-small-awesome-text-to-sql](https://huggingface.co/cssupport/t5-small-awesome-text-to-sql) on huggingface.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
