# Reference
## ApiKeys
<details><summary><code>client.api_keys.<a href="src/streak_crm/api_keys/client.py">list_api_keys</a>(...) -> typing.List[ApiKey]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Lists API keys owned by the current user
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from streak_crm import Streak
from streak_crm.environment import StreakEnvironment

client = Streak(
    token="<token>",
    environment=StreakEnvironment.DEFAULT,
)

client.api_keys.list_api_keys()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**limit:** `typing.Optional[int]` — Number of items to return.
    
</dd>
</dl>

<dl>
<dd>

**page:** `typing.Optional[int]` — Zero-based page number
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.api_keys.<a href="src/streak_crm/api_keys/client.py">create_api_key</a>(...) -> ApiKey</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Creates an API key for the current user
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from streak_crm import Streak
from streak_crm.environment import StreakEnvironment

client = Streak(
    token="<token>",
    environment=StreakEnvironment.DEFAULT,
)

client.api_keys.create_api_key()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**team_key:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.api_keys.<a href="src/streak_crm/api_keys/client.py">delete_api_key</a>(...) -> OperationResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Deletes an API key by key
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from streak_crm import Streak
from streak_crm.environment import StreakEnvironment

client = Streak(
    token="<token>",
    environment=StreakEnvironment.DEFAULT,
)

client.api_keys.delete_api_key(
    api_key_key="apiKeyKey",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**api_key_key:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Boxes
<details><summary><code>client.boxes.<a href="src/streak_crm/boxes/client.py">get_box_markdown</a>(...) -> str</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns the box as one markdown document: an overview, its columns, contacts, organizations, linked boxes, tasks and pipeline, followed by its timeline. Every timestamp is ISO-8601 UTC. The document's structure is best-effort and may change; use the JSON endpoints for a stable contract.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from streak_crm import Streak
from streak_crm.environment import StreakEnvironment

client = Streak(
    token="<token>",
    environment=StreakEnvironment.DEFAULT,
)

client.boxes.get_box_markdown(
    box_key="boxKey",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**box_key:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**max_tokens:** `typing.Optional[int]` — A token cap for the entire document, counted with OpenAI's o200k_base encoding. It covers the box sections first, then uses the remaining tokens for the timeline. A marker shows where entries were left out. If the box does not fit under the cap, a 400 error shows the minimum it needs. Omit the cap to return the full box.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Pipeline
<details><summary><code>client.pipeline.<a href="src/streak_crm/pipeline/client.py">list_pipeline_fields</a>(...) -> typing.List[PipelineField]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns the fields in a pipeline in their stored order.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from streak_crm import Streak
from streak_crm.environment import StreakEnvironment

client = Streak(
    token="<token>",
    environment=StreakEnvironment.DEFAULT,
)

client.pipeline.list_pipeline_fields(
    pipeline_key="pipelineKey",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**pipeline_key:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.pipeline.<a href="src/streak_crm/pipeline/client.py">get_pipeline_field</a>(...) -> PipelineField</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns a field by its key within a pipeline.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from streak_crm import Streak
from streak_crm.environment import StreakEnvironment

client = Streak(
    token="<token>",
    environment=StreakEnvironment.DEFAULT,
)

client.pipeline.get_pipeline_field(
    pipeline_key="pipelineKey",
    field_key="fieldKey",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**pipeline_key:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**field_key:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.pipeline.<a href="src/streak_crm/pipeline/client.py">update_pipeline_field</a>(...) -> PipelineField</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Updates a field's name, default value, options, or AI settings.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from streak_crm import Streak
from streak_crm.environment import StreakEnvironment

client = Streak(
    token="<token>",
    environment=StreakEnvironment.DEFAULT,
)

client.pipeline.update_pipeline_field(
    pipeline_key="pipelineKey",
    field_key="fieldKey",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**pipeline_key:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**field_key:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**add_only:** `typing.Optional[bool]` — Append dropdown or tag options while retaining existing options. Defaults to false.
    
</dd>
</dl>

<dl>
<dd>

**name:** `typing.Optional[str]` — New field name.
    
</dd>
</dl>

<dl>
<dd>

**default_value:** `typing.Optional[str]` — New default value or formula.
    
</dd>
</dl>

<dl>
<dd>

**dropdown_settings:** `typing.Optional[PipelineFieldDropdownSettingsUpdate]` — Dropdown options to apply.
    
</dd>
</dl>

<dl>
<dd>

**tag_settings:** `typing.Optional[PipelineFieldTagSettingsUpdate]` — Tag options to apply.
    
</dd>
</dl>

<dl>
<dd>

**ai_settings:** `typing.Optional[PipelineFieldAiSettingsUpdate]` — AI settings to update.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.pipeline.<a href="src/streak_crm/pipeline/client.py">delete_pipeline_field</a>(...) -> OperationResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Deletes a custom field and clears the value from all the pipeline's boxes.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from streak_crm import Streak
from streak_crm.environment import StreakEnvironment

client = Streak(
    token="<token>",
    environment=StreakEnvironment.DEFAULT,
)

client.pipeline.delete_pipeline_field(
    pipeline_key="pipelineKey",
    field_key="fieldKey",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**pipeline_key:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**field_key:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.pipeline.<a href="src/streak_crm/pipeline/client.py">list_pipelines</a>(...) -> PipelineListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Lists pipelines accessible to the current user.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from streak_crm import Streak
from streak_crm.environment import StreakEnvironment

client = Streak(
    token="<token>",
    environment=StreakEnvironment.DEFAULT,
)

client.pipeline.list_pipelines()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sort_by:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**limit:** `typing.Optional[int]` — Number of items to return.
    
</dd>
</dl>

<dl>
<dd>

**page:** `typing.Optional[int]` — Zero-based page number
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.pipeline.<a href="src/streak_crm/pipeline/client.py">create_pipeline</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Creates a basic pipeline.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from streak_crm import Streak
from streak_crm.environment import StreakEnvironment

client = Streak(
    token="<token>",
    environment=StreakEnvironment.DEFAULT,
)

client.pipeline.create_pipeline(
    name="name",
    team_key="teamKey",
    stages=[
        "stages"
    ],
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**name:** `str` — Pipeline name.
    
</dd>
</dl>

<dl>
<dd>

**team_key:** `str` — Key for the team that will own the pipeline.
    
</dd>
</dl>

<dl>
<dd>

**stages:** `typing.List[str]` — Stage names in display order.
    
</dd>
</dl>

<dl>
<dd>

**icon:** `typing.Optional[str]` — Pipeline icon name.
    
</dd>
</dl>

<dl>
<dd>

**description:** `typing.Optional[str]` — Pipeline description.
    
</dd>
</dl>

<dl>
<dd>

**template_type:** `typing.Optional[str]` — Template identifier associated with the pipeline.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `typing.Optional[typing.List[PipelineFieldCreate]]` — Fields to create in the pipeline.
    
</dd>
</dl>

<dl>
<dd>

**default_permission_set_name:** `typing.Optional[str]` — Default permission set for users without an explicit assignment.
    
</dd>
</dl>

<dl>
<dd>

**sharing_restricted_to_team:** `typing.Optional[bool]` — Whether sharing is restricted to members of the owning team.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.pipeline.<a href="src/streak_crm/pipeline/client.py">get_pipeline</a>(...) -> Pipeline</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns a pipeline by key.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from streak_crm import Streak
from streak_crm.environment import StreakEnvironment

client = Streak(
    token="<token>",
    environment=StreakEnvironment.DEFAULT,
)

client.pipeline.get_pipeline(
    pipeline_key="pipelineKey",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**pipeline_key:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.pipeline.<a href="src/streak_crm/pipeline/client.py">update_pipeline</a>(...) -> Pipeline</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Updates the supplied Pipeline fields. Omitted fields remain unchanged.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from streak_crm import Streak
from streak_crm.environment import StreakEnvironment

client = Streak(
    token="<token>",
    environment=StreakEnvironment.DEFAULT,
)

client.pipeline.update_pipeline(
    pipeline_key="pipelineKey",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**pipeline_key:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**team_key:** `typing.Optional[str]` — New team key. Omit to keep the current team.
    
</dd>
</dl>

<dl>
<dd>

**icon:** `typing.Optional[str]` — New icon. Omit to keep the current icon.
    
</dd>
</dl>

<dl>
<dd>

**name:** `typing.Optional[str]` — New name. Omit to keep the current name.
    
</dd>
</dl>

<dl>
<dd>

**description:** `typing.Optional[str]` — New description. Omit to keep the current description.
    
</dd>
</dl>

<dl>
<dd>

**sharing_restricted_to_team:** `typing.Optional[bool]` — New team sharing restriction. Omit to keep the current value.
    
</dd>
</dl>

<dl>
<dd>

**stage_order:** `typing.Optional[typing.List[str]]` — Complete stage order. Omit to keep the current order; an empty list is invalid.
    
</dd>
</dl>

<dl>
<dd>

**stage_color_theme:** `typing.Optional[str]` — New stage color theme. Omit to keep the current theme.
    
</dd>
</dl>

<dl>
<dd>

**custom_permission_sets:** `typing.Optional[typing.Dict[str, typing.Optional[PipelinePermissionSetInput]]]` — Replacement custom permission sets. Omit to keep existing sets.
    
</dd>
</dl>

<dl>
<dd>

**default_permission_set_name:** `typing.Optional[str]` — New default permission set. Omit to keep the current value.
    
</dd>
</dl>

<dl>
<dd>

**acl_entries:** `typing.Optional[typing.List[PipelineSharingEntryInput]]` — Replacement sharing entries. Omit to keep existing sharing; an empty list is invalid.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.pipeline.<a href="src/streak_crm/pipeline/client.py">delete_pipeline</a>(...) -> OperationResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Deletes an empty pipeline.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from streak_crm import Streak
from streak_crm.environment import StreakEnvironment

client = Streak(
    token="<token>",
    environment=StreakEnvironment.DEFAULT,
)

client.pipeline.delete_pipeline(
    pipeline_key="pipelineKey",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**pipeline_key:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.pipeline.<a href="src/streak_crm/pipeline/client.py">create_pipeline_field</a>(...) -> PipelineField</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Creates a custom field in a pipeline.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from streak_crm import Streak
from streak_crm.environment import StreakEnvironment

client = Streak(
    token="<token>",
    environment=StreakEnvironment.DEFAULT,
)

client.pipeline.create_pipeline_field(
    pipeline_key="pipelineKey",
    name="name",
    type="TEXT_INPUT",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**pipeline_key:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**request:** `PipelineFieldCreate` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Search
<details><summary><code>client.search.<a href="src/streak_crm/search/client.py">search_boxes_contacts_and_organizations</a>(...) -> SearchResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Searches visible boxes, contacts, and organizations by query, or visible boxes by exact name. Exactly one of query or name must be provided.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from streak_crm import Streak
from streak_crm.environment import StreakEnvironment

client = Streak(
    token="<token>",
    environment=StreakEnvironment.DEFAULT,
)

client.search.search_boxes_contacts_and_organizations()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**name:** `typing.Optional[str]` — Exact box name to search for.
    
</dd>
</dl>

<dl>
<dd>

**page:** `typing.Optional[int]` — Zero-based page number.
    
</dd>
</dl>

<dl>
<dd>

**pipeline_key:** `typing.Optional[typing.List[str]]` — Pipeline keys to constrain the search to.
    
</dd>
</dl>

<dl>
<dd>

**query:** `typing.Optional[str]` — Full-text query to search across boxes, contacts, and organizations.
    
</dd>
</dl>

<dl>
<dd>

**stage_key:** `typing.Optional[typing.List[str]]` — Stage keys to constrain the search to.
    
</dd>
</dl>

<dl>
<dd>

**team_key:** `typing.Optional[typing.List[str]]` — Team keys to constrain the search to.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Users
<details><summary><code>client.users.<a href="src/streak_crm/users/client.py">get_current_user</a>() -> User</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns information about the currently authenticated user
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from streak_crm import Streak
from streak_crm.environment import StreakEnvironment

client = Streak(
    token="<token>",
    environment=StreakEnvironment.DEFAULT,
)

client.users.get_current_user()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.users.<a href="src/streak_crm/users/client.py">get_user_by_key</a>(...) -> User</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns information about a specific user by their key
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from streak_crm import Streak
from streak_crm.environment import StreakEnvironment

client = Streak(
    token="<token>",
    environment=StreakEnvironment.DEFAULT,
)

client.users.get_user_by_key(
    user_key="userKey",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_key:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.users.<a href="src/streak_crm/users/client.py">update_user_by_key</a>(...) -> User</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Updates a specific user by their key
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from streak_crm import Streak
from streak_crm.environment import StreakEnvironment

client = Streak(
    token="<token>",
    environment=StreakEnvironment.DEFAULT,
)

client.users.update_user_by_key(
    user_key="userKey",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_key:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**timezone_id:** `typing.Optional[str]` — IANA timezone identifier for the user, such as America/Los_Angeles.
    
</dd>
</dl>

<dl>
<dd>

**first_name:** `typing.Optional[str]` — Given name for the user.
    
</dd>
</dl>

<dl>
<dd>

**last_name:** `typing.Optional[str]` — Family name for the user.
    
</dd>
</dl>

<dl>
<dd>

**automatically_send_invoice_emails:** `typing.Optional[bool]` — Whether invoice emails should be sent automatically.
    
</dd>
</dl>

<dl>
<dd>

**emails_to_send_invoice_to:** `typing.Optional[typing.List[str]]` — Who should receive invoices
    
</dd>
</dl>

<dl>
<dd>

**customer_specified_invoice_data:** `typing.Optional[str]` — Custom data that should be shown on the invoice
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.users.<a href="src/streak_crm/users/client.py">get_all_users_on_team</a>(...) -> UserListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns all the users on a single team including archived users, payer only users, agents, owners and regular members.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from streak_crm import Streak
from streak_crm.environment import StreakEnvironment

client = Streak(
    token="<token>",
    environment=StreakEnvironment.DEFAULT,
)

client.users.get_all_users_on_team(
    team_key="teamKey",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**team_key:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Comments
<details><summary><code>client.comments.<a href="src/streak_crm/comments/client.py">list_comments</a>(...) -> CommentListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Lists comments on a box
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from streak_crm import Streak
from streak_crm.environment import StreakEnvironment

client = Streak(
    token="<token>",
    environment=StreakEnvironment.DEFAULT,
)

client.comments.list_comments(
    box_key="boxKey",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**box_key:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.comments.<a href="src/streak_crm/comments/client.py">create_comment</a>(...) -> Comment</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Creates a comment on a box
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from streak_crm import Streak
from streak_crm.environment import StreakEnvironment

client = Streak(
    token="<token>",
    environment=StreakEnvironment.DEFAULT,
)

client.comments.create_comment(
    box_key="boxKey",
    message="message",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**box_key:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**message:** `str` — Comment text.
    
</dd>
</dl>

<dl>
<dd>

**mentions:** `typing.Optional[typing.List[CommentMentionBody]]` — Mention ranges in the comment text.
    
</dd>
</dl>

<dl>
<dd>

**parent:** `typing.Optional[str]` — Parent comment key when creating a reply.
    
</dd>
</dl>

<dl>
<dd>

**search_for_at_mentions:** `typing.Optional[bool]` — Whether to scan the comment text for unstructured @mentions of users display name, first name or email address.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.comments.<a href="src/streak_crm/comments/client.py">get_comment</a>(...) -> Comment</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns a comment by key
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from streak_crm import Streak
from streak_crm.environment import StreakEnvironment

client = Streak(
    token="<token>",
    environment=StreakEnvironment.DEFAULT,
)

client.comments.get_comment(
    comment_key="commentKey",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**comment_key:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.comments.<a href="src/streak_crm/comments/client.py">update_comment</a>(...) -> Comment</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Updates a comment by key
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from streak_crm import Streak
from streak_crm.environment import StreakEnvironment

client = Streak(
    token="<token>",
    environment=StreakEnvironment.DEFAULT,
)

client.comments.update_comment(
    comment_key="commentKey",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**comment_key:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**message:** `typing.Optional[str]` — New comment text. Omit this field to keep the existing comment text unchanged.
    
</dd>
</dl>

<dl>
<dd>

**mentions:** `typing.Optional[typing.List[CommentMentionBody]]` — New mention ranges for the comment text. Omit this field to keep existing mentions unchanged.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.comments.<a href="src/streak_crm/comments/client.py">delete_comment</a>(...) -> OperationResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Deletes a comment by key
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from streak_crm import Streak
from streak_crm.environment import StreakEnvironment

client = Streak(
    token="<token>",
    environment=StreakEnvironment.DEFAULT,
)

client.comments.delete_comment(
    comment_key="commentKey",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**comment_key:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.comments.<a href="src/streak_crm/comments/client.py">react_to_comment</a>(...) -> Comment</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Adds an emoji reaction to a comment
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from streak_crm import Streak
from streak_crm.environment import StreakEnvironment

client = Streak(
    token="<token>",
    environment=StreakEnvironment.DEFAULT,
)

client.comments.react_to_comment(
    comment_key="commentKey",
    emoji="emoji",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**comment_key:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**request:** `CommentReactionBody` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.comments.<a href="src/streak_crm/comments/client.py">remove_comment_reaction</a>(...) -> Comment</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Removes an emoji reaction from a comment
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from streak_crm import Streak
from streak_crm.environment import StreakEnvironment

client = Streak(
    token="<token>",
    environment=StreakEnvironment.DEFAULT,
)

client.comments.remove_comment_reaction(
    comment_key="commentKey",
    emoji="emoji",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**comment_key:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**request:** `CommentReactionBody` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Meetings
<details><summary><code>client.meetings.<a href="src/streak_crm/meetings/client.py">list_meetings</a>(...) -> MeetingListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Lists meetings and call logs on a box
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from streak_crm import Streak
from streak_crm.environment import StreakEnvironment

client = Streak(
    token="<token>",
    environment=StreakEnvironment.DEFAULT,
)

client.meetings.list_meetings(
    box_key="boxKey",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**box_key:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**limit:** `typing.Optional[int]` — Number of items to return.
    
</dd>
</dl>

<dl>
<dd>

**page:** `typing.Optional[int]` — Zero-based page number
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.meetings.<a href="src/streak_crm/meetings/client.py">create_meeting</a>(...) -> Meeting</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Creates a meeting or call log on a box
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from streak_crm import Streak
from streak_crm.environment import StreakEnvironment

client = Streak(
    token="<token>",
    environment=StreakEnvironment.DEFAULT,
)

client.meetings.create_meeting(
    box_key="boxKey",
    meeting_type="CALL_LOG",
    start_timestamp=1646870400000,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**box_key:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**meeting_type:** `MeetingType` — Meeting type.
    
</dd>
</dl>

<dl>
<dd>

**start_timestamp:** `int` — Meeting start timestamp, in epoch milliseconds.
    
</dd>
</dl>

<dl>
<dd>

**duration:** `typing.Optional[int]` — Meeting duration in milliseconds.
    
</dd>
</dl>

<dl>
<dd>

**notes:** `typing.Optional[str]` — Meeting notes.
    
</dd>
</dl>

<dl>
<dd>

**task_keys:** `typing.Optional[typing.List[str]]` — Task keys associated with this meeting.
    
</dd>
</dl>

<dl>
<dd>

**is_draft:** `typing.Optional[bool]` — Whether this meeting is a draft.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.meetings.<a href="src/streak_crm/meetings/client.py">get_meeting</a>(...) -> Meeting</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns a meeting or call log by key
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from streak_crm import Streak
from streak_crm.environment import StreakEnvironment

client = Streak(
    token="<token>",
    environment=StreakEnvironment.DEFAULT,
)

client.meetings.get_meeting(
    meeting_key="meetingKey",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**meeting_key:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.meetings.<a href="src/streak_crm/meetings/client.py">update_meeting</a>(...) -> Meeting</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Updates a meeting or call log by key
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from streak_crm import Streak
from streak_crm.environment import StreakEnvironment

client = Streak(
    token="<token>",
    environment=StreakEnvironment.DEFAULT,
)

client.meetings.update_meeting(
    meeting_key="meetingKey",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**meeting_key:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**meeting_type:** `typing.Optional[str]` — New meeting type. Omit this field to keep the existing meeting type unchanged.
    
</dd>
</dl>

<dl>
<dd>

**start_timestamp:** `typing.Optional[int]` — New meeting start timestamp, in epoch milliseconds. Omit this field to keep the existing start time unchanged.
    
</dd>
</dl>

<dl>
<dd>

**duration:** `typing.Optional[int]` — New meeting duration in milliseconds. Omit this field to keep the existing duration unchanged.
    
</dd>
</dl>

<dl>
<dd>

**notes:** `typing.Optional[str]` — New meeting notes. Omit this field to keep the existing notes unchanged.
    
</dd>
</dl>

<dl>
<dd>

**is_draft:** `typing.Optional[bool]` — Whether to publish a draft meeting. Omit this field to keep the existing draft state unchanged.
    
</dd>
</dl>

<dl>
<dd>

**task_keys:** `typing.Optional[typing.List[str]]` — Replacement task keys associated with this meeting. Omit this field to keep existing task keys unchanged.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.meetings.<a href="src/streak_crm/meetings/client.py">delete_meeting</a>(...) -> OperationResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Deletes a meeting or call log by key
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from streak_crm import Streak
from streak_crm.environment import StreakEnvironment

client = Streak(
    token="<token>",
    environment=StreakEnvironment.DEFAULT,
)

client.meetings.delete_meeting(
    meeting_key="meetingKey",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**meeting_key:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Tasks
<details><summary><code>client.tasks.<a href="src/streak_crm/tasks/client.py">list_box_tasks</a>(...) -> TaskListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Lists tasks on a box, ordered by creation date.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from streak_crm import Streak
from streak_crm.environment import StreakEnvironment

client = Streak(
    token="<token>",
    environment=StreakEnvironment.DEFAULT,
)

client.tasks.list_box_tasks(
    box_key="boxKey",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**box_key:** `str` — Key for the box whose tasks should be listed.
    
</dd>
</dl>

<dl>
<dd>

**limit:** `typing.Optional[int]` — Number of items to return. Maximum: 1000
    
</dd>
</dl>

<dl>
<dd>

**page:** `typing.Optional[int]` — Zero-based page number
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.tasks.<a href="src/streak_crm/tasks/client.py">create_task</a>(...) -> Task</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Creates a task on a box.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from streak_crm import Streak
from streak_crm.environment import StreakEnvironment

client = Streak(
    token="<token>",
    environment=StreakEnvironment.DEFAULT,
)

client.tasks.create_task(
    box_key="boxKey",
    text="text",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**box_key:** `str` — Key for the box to create the task on.
    
</dd>
</dl>

<dl>
<dd>

**text:** `str` — Task text.
    
</dd>
</dl>

<dl>
<dd>

**due_date:** `typing.Optional[int]` — Task due date, in epoch milliseconds. Use -1 to create a task with no due date.
    
</dd>
</dl>

<dl>
<dd>

**assigned_to:** `typing.Optional[typing.List[AssigneeInput]]` — Users to assign to this task. Omit to assign the task to the creator.
    
</dd>
</dl>

<dl>
<dd>

**meeting_key:** `typing.Optional[str]` — Key for the meeting this task belongs to, when any.
    
</dd>
</dl>

<dl>
<dd>

**is_draft:** `typing.Optional[bool]` — Whether to create this task as a draft. Draft tasks do not send notifications or webhooks.
    
</dd>
</dl>

<dl>
<dd>

**team_contact_key:** `typing.Optional[str]` — Key for the contact used to infer suggested task actions.
    
</dd>
</dl>

<dl>
<dd>

**draft:** `typing.Optional[bool]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.tasks.<a href="src/streak_crm/tasks/client.py">list_upcoming_tasks</a>(...) -> TaskListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Lists tasks across all pipelines and boxes. By default, returns incomplete tasks assigned to the current user before tomorrow in the user's timezone, which includes today's and overdue tasks. Use userKeys, pipelineKey, includeCompleted, direction, limit, and sortOrder to page through other agenda slices.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from streak_crm import Streak
from streak_crm.environment import StreakEnvironment

client = Streak(
    token="<token>",
    environment=StreakEnvironment.DEFAULT,
)

client.tasks.list_upcoming_tasks()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**direction:** `typing.Optional[str]` — Agenda direction. Accepted values are desc, past, asc, and future. Defaults to desc.
    
</dd>
</dl>

<dl>
<dd>

**include_completed:** `typing.Optional[bool]` — Whether completed tasks should be included in the returned agenda.
    
</dd>
</dl>

<dl>
<dd>

**limit:** `typing.Optional[int]` — Maximum number of tasks to return per assigned user.
    
</dd>
</dl>

<dl>
<dd>

**pipeline_key:** `typing.Optional[str]` — Key for the pipeline to filter tasks to. Omit to search across all visible pipelines.
    
</dd>
</dl>

<dl>
<dd>

**sort_order:** `typing.Optional[str]` — Opaque 30-digit sort cursor returned as task.sortOrder. Omit to use tomorrow at local midnight as the cursor boundary.
    
</dd>
</dl>

<dl>
<dd>

**user_keys:** `typing.Optional[typing.List[str]]` — User keys whose assigned tasks should be returned. Omit to return tasks assigned to the current user.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.tasks.<a href="src/streak_crm/tasks/client.py">get_task</a>(...) -> Task</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns a single task by key.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from streak_crm import Streak
from streak_crm.environment import StreakEnvironment

client = Streak(
    token="<token>",
    environment=StreakEnvironment.DEFAULT,
)

client.tasks.get_task(
    task_key="taskKey",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**task_key:** `str` — Key for the task to return.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.tasks.<a href="src/streak_crm/tasks/client.py">update_task</a>(...) -> Task</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Updates a task by key. Omitted body fields are left unchanged.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from streak_crm import Streak
from streak_crm.environment import StreakEnvironment

client = Streak(
    token="<token>",
    environment=StreakEnvironment.DEFAULT,
)

client.tasks.update_task(
    task_key="taskKey",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**task_key:** `str` — Key for the task to update.
    
</dd>
</dl>

<dl>
<dd>

**text:** `typing.Optional[str]` — New task text. Omit this field to keep existing text unchanged.
    
</dd>
</dl>

<dl>
<dd>

**due_date:** `typing.Optional[int]` — New task due date, in epoch milliseconds. Use -1 to clear the due date.
    
</dd>
</dl>

<dl>
<dd>

**status:** `typing.Optional[str]` — New task completion status. Omit this field to keep existing status unchanged.
    
</dd>
</dl>

<dl>
<dd>

**assigned_to:** `typing.Optional[typing.List[AssigneeInput]]` — Replacement users assigned to this task. Omit this field to keep existing assignees unchanged.
    
</dd>
</dl>

<dl>
<dd>

**meeting_key:** `typing.Optional[str]` — Key for the meeting this task belongs to. Omit this field to keep existing meeting unchanged.
    
</dd>
</dl>

<dl>
<dd>

**is_draft:** `typing.Optional[bool]` — Whether to publish a draft task. Omit this field to keep existing draft state unchanged.
    
</dd>
</dl>

<dl>
<dd>

**draft:** `typing.Optional[bool]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.tasks.<a href="src/streak_crm/tasks/client.py">delete_task</a>(...) -> OperationResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Deletes a task by key.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from streak_crm import Streak
from streak_crm.environment import StreakEnvironment

client = Streak(
    token="<token>",
    environment=StreakEnvironment.DEFAULT,
)

client.tasks.delete_task(
    task_key="taskKey",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**task_key:** `str` — Key for the task to delete.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Contact
<details><summary><code>client.contact.<a href="src/streak_crm/contact/client.py">get_contacts_in_bulk</a>(...) -> ContactKeyBatch</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns accessible contacts indexed by their requested keys. Missing and inaccessible contacts are omitted.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from streak_crm import Streak
from streak_crm.environment import StreakEnvironment

client = Streak(
    token="<token>",
    environment=StreakEnvironment.DEFAULT,
)

client.contact.get_contacts_in_bulk(
    request=[
        "string"
    ],
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `typing.List[str]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.contact.<a href="src/streak_crm/contact/client.py">get_contact</a>(...) -> Contact</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns an accessible contact by key.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from streak_crm import Streak
from streak_crm.environment import StreakEnvironment

client = Streak(
    token="<token>",
    environment=StreakEnvironment.DEFAULT,
)

client.contact.get_contact(
    contact_key="contactKey",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**contact_key:** `str` — Key of the contact.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.contact.<a href="src/streak_crm/contact/client.py">update_contact</a>(...) -> Contact</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Applies supplied changes. Null or omitted fields remain unchanged.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from streak_crm import Streak
from streak_crm.environment import StreakEnvironment

client = Streak(
    token="<token>",
    environment=StreakEnvironment.DEFAULT,
)

client.contact.update_contact(
    contact_key="contactKey",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**contact_key:** `str` — Key of the contact.
    
</dd>
</dl>

<dl>
<dd>

**given_name:** `typing.Optional[str]` — New given name; an empty string clears it if another identifier remains.
    
</dd>
</dl>

<dl>
<dd>

**family_name:** `typing.Optional[str]` — New family name; an empty string clears it if another identifier remains.
    
</dd>
</dl>

<dl>
<dd>

**title:** `typing.Optional[str]` — New job title; an empty string clears it.
    
</dd>
</dl>

<dl>
<dd>

**other:** `typing.Optional[str]` — New notes; an empty string clears them.
    
</dd>
</dl>

<dl>
<dd>

**email_addresses:** `typing.Optional[typing.List[str]]` — Replacement email addresses; a contact must retain an email address or a name.
    
</dd>
</dl>

<dl>
<dd>

**phone_numbers:** `typing.Optional[typing.List[str]]` — Replacement phone numbers. Empty entries are removed.
    
</dd>
</dl>

<dl>
<dd>

**addresses:** `typing.Optional[typing.List[str]]` — Replacement postal addresses. Empty entries are removed.
    
</dd>
</dl>

<dl>
<dd>

**domains:** `typing.Optional[typing.List[str]]` — Replacement website domains.
    
</dd>
</dl>

<dl>
<dd>

**twitter_handle:** `typing.Optional[str]` — Replacement Twitter handle.
    
</dd>
</dl>

<dl>
<dd>

**facebook_handle:** `typing.Optional[str]` — Replacement Facebook handle.
    
</dd>
</dl>

<dl>
<dd>

**linkedin_handle:** `typing.Optional[str]` — Replacement LinkedIn handle.
    
</dd>
</dl>

<dl>
<dd>

**instagram_handle:** `typing.Optional[str]` — Replacement Instagram handle.
    
</dd>
</dl>

<dl>
<dd>

**photo_url:** `typing.Optional[str]` — Replacement photo URL.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `typing.Optional[typing.Dict[str, typing.Optional[str]]]` — Custom-field values to merge by field key. Null entries are ignored; an empty map leaves existing fields unchanged.
    
</dd>
</dl>

<dl>
<dd>

**contact_links:** `typing.Optional[typing.List[ContactLinkInput]]` — Replacement links to contacts; an empty list removes the links.
    
</dd>
</dl>

<dl>
<dd>

**org_links:** `typing.Optional[typing.List[OrganizationLinkInput]]` — Replacement links to organizations; an empty list removes the links.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.contact.<a href="src/streak_crm/contact/client.py">delete_contact</a>(...) -> OperationResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Deletes a contact and schedules cleanup of its links. A missing contact returns 404.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from streak_crm import Streak
from streak_crm.environment import StreakEnvironment

client = Streak(
    token="<token>",
    environment=StreakEnvironment.DEFAULT,
)

client.contact.delete_contact(
    contact_key="contactKey",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**contact_key:** `str` — Key of the contact.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.contact.<a href="src/streak_crm/contact/client.py">list_contacts</a>(...) -> ContactPage</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Lists contacts in stable order. Pass the returned cursor to continue; keep the same after filter across pages. A full last page may be followed by an empty page.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from streak_crm import Streak
from streak_crm.environment import StreakEnvironment

client = Streak(
    token="<token>",
    environment=StreakEnvironment.DEFAULT,
)

client.contact.list_contacts(
    team_key="teamKey",
    after=1646870400,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**team_key:** `str` — Key of the team.
    
</dd>
</dl>

<dl>
<dd>

**after:** `typing.Optional[int]` — Include contacts last saved at or after this epoch-seconds timestamp.
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` — Cursor returned by the previous response. Omit or leave blank to start from the beginning.
    
</dd>
</dl>

<dl>
<dd>

**limit:** `typing.Optional[int]` — Maximum number of results to return. Defaults to 100. Values above 1000 are capped.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.contact.<a href="src/streak_crm/contact/client.py">create_contact</a>(...) -> Contact</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Creates a contact from its basic details. Links and custom fields require a subsequent update.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from streak_crm import Streak
from streak_crm.environment import StreakEnvironment

client = Streak(
    token="<token>",
    environment=StreakEnvironment.DEFAULT,
)

client.contact.create_contact(
    team_key="teamKey",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**team_key:** `str` — Key of the team.
    
</dd>
</dl>

<dl>
<dd>

**get_if_existing:** `typing.Optional[bool]` — Return an existing email match instead of creating a contact. When getIfExisting=true, an email match is returned without merging new values.
    
</dd>
</dl>

<dl>
<dd>

**given_name:** `typing.Optional[str]` — Given name.
    
</dd>
</dl>

<dl>
<dd>

**family_name:** `typing.Optional[str]` — Family name.
    
</dd>
</dl>

<dl>
<dd>

**title:** `typing.Optional[str]` — Job title.
    
</dd>
</dl>

<dl>
<dd>

**other:** `typing.Optional[str]` — Additional notes about the contact.
    
</dd>
</dl>

<dl>
<dd>

**email_addresses:** `typing.Optional[typing.List[str]]` — Email addresses for the contact.
    
</dd>
</dl>

<dl>
<dd>

**phone_numbers:** `typing.Optional[typing.List[str]]` — Phone numbers for the contact.
    
</dd>
</dl>

<dl>
<dd>

**addresses:** `typing.Optional[typing.List[str]]` — Postal addresses for the contact.
    
</dd>
</dl>

<dl>
<dd>

**domains:** `typing.Optional[typing.List[str]]` — Website domains associated with the contact.
    
</dd>
</dl>

<dl>
<dd>

**twitter_handle:** `typing.Optional[str]` — Twitter handle.
    
</dd>
</dl>

<dl>
<dd>

**facebook_handle:** `typing.Optional[str]` — Facebook handle.
    
</dd>
</dl>

<dl>
<dd>

**linkedin_handle:** `typing.Optional[str]` — LinkedIn handle.
    
</dd>
</dl>

<dl>
<dd>

**instagram_handle:** `typing.Optional[str]` — Instagram handle.
    
</dd>
</dl>

<dl>
<dd>

**photo_url:** `typing.Optional[str]` — URL for the contact's photo.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Organization
<details><summary><code>client.organization.<a href="src/streak_crm/organization/client.py">get_organizations_in_a_batch</a>(...) -> typing.Dict[str, Organization]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns organizations keyed by their organization keys. Missing and inaccessible organizations are omitted.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from streak_crm import Streak
from streak_crm.environment import StreakEnvironment

client = Streak(
    token="<token>",
    environment=StreakEnvironment.DEFAULT,
)

client.organization.get_organizations_in_a_batch(
    request=[
        "string"
    ],
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `typing.List[str]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.organization.<a href="src/streak_crm/organization/client.py">get_an_organization</a>(...) -> Organization</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns an organization accessible to the current user, including custom fields and relationships.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from streak_crm import Streak
from streak_crm.environment import StreakEnvironment

client = Streak(
    token="<token>",
    environment=StreakEnvironment.DEFAULT,
)

client.organization.get_an_organization(
    organization_key="organizationKey",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**organization_key:** `str` — Key of the organization.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.organization.<a href="src/streak_crm/organization/client.py">update_an_organization</a>(...) -> Organization</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Updates an organization. Omitted and null properties are unchanged. Supplied lists replace existing lists, subject to field validation.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from streak_crm import Streak
from streak_crm.environment import StreakEnvironment

client = Streak(
    token="<token>",
    environment=StreakEnvironment.DEFAULT,
)

client.organization.update_an_organization(
    organization_key="organizationKey",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**organization_key:** `str` — Key of the organization.
    
</dd>
</dl>

<dl>
<dd>

**name:** `typing.Optional[str]` — Replacement organization name. A name or domain must remain after the update.
    
</dd>
</dl>

<dl>
<dd>

**other:** `typing.Optional[str]` — Replacement notes. An empty string clears the notes.
    
</dd>
</dl>

<dl>
<dd>

**domains:** `typing.Optional[typing.List[str]]` — Replacement domains, with the primary domain first. An empty list clears domains if a name remains.
    
</dd>
</dl>

<dl>
<dd>

**industry:** `typing.Optional[str]` — Replacement industry.
    
</dd>
</dl>

<dl>
<dd>

**phone_numbers:** `typing.Optional[typing.List[str]]` — Replacement phone numbers. An empty list clears existing phone numbers.
    
</dd>
</dl>

<dl>
<dd>

**addresses:** `typing.Optional[typing.List[str]]` — Replacement postal addresses. An empty list clears existing addresses.
    
</dd>
</dl>

<dl>
<dd>

**employee_count:** `typing.Optional[str]` — Replacement company size as text, including employee-count ranges.
    
</dd>
</dl>

<dl>
<dd>

**logo_url:** `typing.Optional[str]` — Replacement organization logo URL.
    
</dd>
</dl>

<dl>
<dd>

**twitter_handle:** `typing.Optional[str]` — Replacement Twitter profile handle or URL.
    
</dd>
</dl>

<dl>
<dd>

**facebook_handle:** `typing.Optional[str]` — Replacement Facebook profile handle or URL.
    
</dd>
</dl>

<dl>
<dd>

**linkedin_handle:** `typing.Optional[str]` — Replacement LinkedIn profile handle or URL.
    
</dd>
</dl>

<dl>
<dd>

**instagram_handle:** `typing.Optional[str]` — Replacement Instagram profile handle or URL.
    
</dd>
</dl>

<dl>
<dd>

**contact_links:** `typing.Optional[typing.List[ContactLinkInput]]` — Replacement contact relationships. An empty list removes existing relationships.
    
</dd>
</dl>

<dl>
<dd>

**org_links:** `typing.Optional[typing.List[OrganizationLinkInput]]` — Replacement organization relationships. An empty list removes existing relationships.
    
</dd>
</dl>

<dl>
<dd>

**fields:** `typing.Optional[typing.Dict[str, typing.Optional[str]]]` — Custom field values to change, keyed by field ID. Omitted keys and null values are unchanged; an empty object makes no changes.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.organization.<a href="src/streak_crm/organization/client.py">delete_an_organization</a>(...) -> OperationResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Deletes an organization and schedules removal of its relationships and box links.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from streak_crm import Streak
from streak_crm.environment import StreakEnvironment

client = Streak(
    token="<token>",
    environment=StreakEnvironment.DEFAULT,
)

client.organization.delete_an_organization(
    organization_key="organizationKey",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**organization_key:** `str` — Key of the organization.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.organization.<a href="src/streak_crm/organization/client.py">list_organizations</a>(...) -> OrganizationPage</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns organizations in a team, ordered by key. Pass the returned cursor to retrieve the next page.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from streak_crm import Streak
from streak_crm.environment import StreakEnvironment

client = Streak(
    token="<token>",
    environment=StreakEnvironment.DEFAULT,
)

client.organization.list_organizations(
    team_key="teamKey",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**team_key:** `str` — Key of the team.
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` — Cursor returned by the previous response. Omit or leave blank to start from the beginning.
    
</dd>
</dl>

<dl>
<dd>

**limit:** `typing.Optional[int]` — Maximum number of results to return. Defaults to 100. Values above 1000 are capped.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.organization.<a href="src/streak_crm/organization/client.py">create_an_organization</a>(...) -> Organization</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Creates an organization in a team. Available enrichment data may fill missing details. Provide a name or at least one domain. Set custom fields and relationships in a subsequent update.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from streak_crm import Streak
from streak_crm.environment import StreakEnvironment

client = Streak(
    token="<token>",
    environment=StreakEnvironment.DEFAULT,
)

client.organization.create_an_organization(
    team_key="teamKey",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**team_key:** `str` — Key of the team.
    
</dd>
</dl>

<dl>
<dd>

**get_if_existing:** `typing.Optional[bool]` — Return an existing organization matching a supplied domain instead of creating another organization. The supplied values are not merged into the existing organization.
    
</dd>
</dl>

<dl>
<dd>

**name:** `typing.Optional[str]` — Organization name.
    
</dd>
</dl>

<dl>
<dd>

**other:** `typing.Optional[str]` — Freeform notes about the organization.
    
</dd>
</dl>

<dl>
<dd>

**domains:** `typing.Optional[typing.List[str]]` — Website domains for the organization, with the primary domain first.
    
</dd>
</dl>

<dl>
<dd>

**industry:** `typing.Optional[str]` — Industry of the organization.
    
</dd>
</dl>

<dl>
<dd>

**phone_numbers:** `typing.Optional[typing.List[str]]` — Phone numbers for the organization.
    
</dd>
</dl>

<dl>
<dd>

**addresses:** `typing.Optional[typing.List[str]]` — Postal addresses for the organization.
    
</dd>
</dl>

<dl>
<dd>

**employee_count:** `typing.Optional[str]` — Company size as text, which can include an employee-count range.
    
</dd>
</dl>

<dl>
<dd>

**logo_url:** `typing.Optional[str]` — URL of the organization's logo.
    
</dd>
</dl>

<dl>
<dd>

**twitter_handle:** `typing.Optional[str]` — Twitter profile handle or URL.
    
</dd>
</dl>

<dl>
<dd>

**facebook_handle:** `typing.Optional[str]` — Facebook profile handle or URL.
    
</dd>
</dl>

<dl>
<dd>

**linkedin_handle:** `typing.Optional[str]` — LinkedIn profile handle or URL.
    
</dd>
</dl>

<dl>
<dd>

**instagram_handle:** `typing.Optional[str]` — Instagram profile handle or URL.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## PipelineStage
<details><summary><code>client.pipeline_stage.<a href="src/streak_crm/pipeline_stage/client.py">list_stages</a>(...) -> typing.Dict[str, PipelineStage]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns the pipeline's stages keyed by stage key.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from streak_crm import Streak
from streak_crm.environment import StreakEnvironment

client = Streak(
    token="<token>",
    environment=StreakEnvironment.DEFAULT,
)

client.pipeline_stage.list_stages(
    pipeline_key="pipelineKey",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**pipeline_key:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.pipeline_stage.<a href="src/streak_crm/pipeline_stage/client.py">create_stage</a>(...) -> PipelineStage</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Creates a stage at the end of the pipeline's stage order.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from streak_crm import Streak
from streak_crm.environment import StreakEnvironment

client = Streak(
    token="<token>",
    environment=StreakEnvironment.DEFAULT,
)

client.pipeline_stage.create_stage(
    pipeline_key="pipelineKey",
    name="name",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**pipeline_key:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**name:** `str` — Nonempty name of the new stage.
    
</dd>
</dl>

<dl>
<dd>

**color:** `typing.Optional[PipelineStageColor]` — Custom stage colors. Omit or set to null to use the pipeline theme.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.pipeline_stage.<a href="src/streak_crm/pipeline_stage/client.py">get_stage</a>(...) -> PipelineStage</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns a stage in a pipeline.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from streak_crm import Streak
from streak_crm.environment import StreakEnvironment

client = Streak(
    token="<token>",
    environment=StreakEnvironment.DEFAULT,
)

client.pipeline_stage.get_stage(
    pipeline_key="pipelineKey",
    stage_key="stageKey",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**pipeline_key:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**stage_key:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.pipeline_stage.<a href="src/streak_crm/pipeline_stage/client.py">update_stage</a>(...) -> PipelineStage</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Updates the supplied stage name or colors.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from streak_crm import Streak
from streak_crm.environment import StreakEnvironment

client = Streak(
    token="<token>",
    environment=StreakEnvironment.DEFAULT,
)

client.pipeline_stage.update_stage(
    pipeline_key="pipelineKey",
    stage_key="stageKey",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**pipeline_key:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**stage_key:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**name:** `typing.Optional[str]` — Nonempty new stage name.
    
</dd>
</dl>

<dl>
<dd>

**color:** `typing.Optional[PipelineStageColor]` — Custom stage colors. Set both foregroundColor and backgroundColor to empty strings to reset to the pipeline theme.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.pipeline_stage.<a href="src/streak_crm/pipeline_stage/client.py">delete_stage</a>(...) -> OperationResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Deletes an empty stage. The final stage in a pipeline cannot be deleted.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from streak_crm import Streak
from streak_crm.environment import StreakEnvironment

client = Streak(
    token="<token>",
    environment=StreakEnvironment.DEFAULT,
)

client.pipeline_stage.delete_stage(
    pipeline_key="pipelineKey",
    stage_key="stageKey",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**pipeline_key:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**stage_key:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Team
<details><summary><code>client.team.<a href="src/streak_crm/team/client.py">create_team</a>(...) -> Team</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Creates a team with an initial member roster.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from streak_crm import Streak, TeamMemberCreate
from streak_crm.environment import StreakEnvironment

client = Streak(
    token="<token>",
    environment=StreakEnvironment.DEFAULT,
)

client.team.create_team(
    name="name",
    members=[
        TeamMemberCreate()
    ],
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**name:** `str` — Display name for the new team.
    
</dd>
</dl>

<dl>
<dd>

**members:** `typing.List[TeamMemberCreate]` — Initial team members. The authenticated creator must be included.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.team.<a href="src/streak_crm/team/client.py">get_team</a>(...) -> Team</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns a team by key.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from streak_crm import Streak
from streak_crm.environment import StreakEnvironment

client = Streak(
    token="<token>",
    environment=StreakEnvironment.DEFAULT,
)

client.team.get_team(
    team_key="teamKey",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**team_key:** `str` — Key for the team to return.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.team.<a href="src/streak_crm/team/client.py">update_team</a>(...) -> Team</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Updates a team by key. Omitted body fields are left unchanged.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from streak_crm import Streak
from streak_crm.environment import StreakEnvironment

client = Streak(
    token="<token>",
    environment=StreakEnvironment.DEFAULT,
)

client.team.update_team(
    team_key="teamKey",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**team_key:** `str` — Key for the team to update.
    
</dd>
</dl>

<dl>
<dd>

**name:** `typing.Optional[str]` — New display name for the team.
    
</dd>
</dl>

<dl>
<dd>

**sharing_restricted_to_team:** `typing.Optional[bool]` — Whether sharing outside the team is restricted.
    
</dd>
</dl>

<dl>
<dd>

**automatically_approve_join_requests:** `typing.Optional[bool]` — Whether requests to join the team are approved automatically.
    
</dd>
</dl>

<dl>
<dd>

**automatically_send_invoice_emails:** `typing.Optional[bool]` — Whether invoice emails are sent automatically for this team.
    
</dd>
</dl>

<dl>
<dd>

**emails_to_send_invoice_to:** `typing.Optional[typing.List[str]]` — Complete replacement for additional invoice-recipient email addresses. Omit to leave unchanged; send an empty set to clear.
    
</dd>
</dl>

<dl>
<dd>

**members:** `typing.Optional[typing.List[TeamMemberUpdate]]` — Complete replacement roster. Omit this property to leave membership unchanged.
    
</dd>
</dl>

<dl>
<dd>

**contact_org_list_permissions:** `typing.Optional[typing.Dict[str, typing.Optional[TeamBasedPermissionsUpdate]]]` — Permission updates keyed by system list. Omitted list entries remain unchanged.
    
</dd>
</dl>

<dl>
<dd>

**contact_settings:** `typing.Optional[TeamFieldSettingsUpdate]` — Complete replacement for the team's custom contact fields. Omit to leave unchanged.
    
</dd>
</dl>

<dl>
<dd>

**organization_settings:** `typing.Optional[TeamFieldSettingsUpdate]` — Complete replacement for the team's custom organization fields. Omit to leave unchanged.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.team.<a href="src/streak_crm/team/client.py">list_current_users_teams</a>(...) -> TeamListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Lists the teams the current user belongs to, newest first.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from streak_crm import Streak
from streak_crm.environment import StreakEnvironment

client = Streak(
    token="<token>",
    environment=StreakEnvironment.DEFAULT,
)

client.team.list_current_users_teams()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**limit:** `typing.Optional[int]` — Number of items to return.
    
</dd>
</dl>

<dl>
<dd>

**page:** `typing.Optional[int]` — Zero-based page number
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

