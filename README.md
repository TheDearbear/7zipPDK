## 7-zip Plugin Development Kit
7zipPDK will allow you to write and compile external codecs and formats for 7zip soon™

### Full Exports List
 - [CreateObject](#createobject)
 - CreateDecoder
 - CreateEncoder
 - [GetNumberOfMethods](#getnumberofmethods)
 - [GetNumberOfFormats](#getnumberofformats)
 - [GetMethodProperty](#getmethodproperty)
 - GetHandlerProperty
 - GetHandlerProperty2
 - [GetPluginProperty](#getpluginproperty)
 - GetHashers
 - GetIsArc
 - [SetLargePageMode](#setlargepagemode)
 - [SetCaseSensitive](#setcasesensitive)
 - SetCodecs

### Exports Overview
#### CreateObject
Definition: __HRESULT CreateObject(const GUID \*clsid, const GUID \*iid, [out] void \*\*outObject)__  
Description: Used to create one of the following things: Coder, Hasher, Folder Manager, In/Out Archive Handler, Encoder (if CreateEncoder is not present), Decoder (if CreateDecoder is not present)  
Parameters:
|     Name     |     Type     |     Description    |
| ------------ | ------------ | ------------------ |
| clsid        | GUID \*      | Requested class    |
| iid          | GUID \*      | Requested category |
| outObject    | void \*\*    | Function result    |

------------

#### CreateDecoder
##### Currently WIP
Definition: __HRESULT CreateDecoder(UInt32 index, const GUID \*iid, void \*\*outObject)__  
Description: TBD   
Parameters:
| Name | Type | Description |
| ------------ | ------------ | ------------ |
| index | UInt32 | Decoder id? |
| iid | GUID \* | idk |
| outObject | void ** | Some memory |

------------

#### CreateEncoder
##### Currently WIP
Definition: __HRESULT CreateEncoder(UInt32 index, const GUID \*iid, void \*\*outObject)__  
Description: TDB  
Parameters:
| Name | Type | Description |
| ------------ | ------------ | ------------ |
| index | UInt32 | Encoder id? |
| iid | GUID \* | idk |
| outObject | void ** | Some memory |

------------

#### GetNumberOfMethods
Definition: __HRESULT GetNumberOfMethods([out] UInt32 \*numCodecs)__  
Description: Get number of supported codecs  
Parameters:
|     Name     |      Type       |   Description    |
| ------------ | --------------- | ---------------- |
|   numCodecs  | unsigned int \* | Number of codecs |

------------

#### GetNumberOfFormats
Definition: __HRESULT GetNumberOfFormats([out] UInt32 \*numFormats)__  
Description: Get number of supported formats  
Parameters:
|     Name     |       Type      |    Description    |
| ------------ | --------------- | ----------------- |
|  numFormats  | unsigned int \* | Number of formats |

------------

#### GetMethodProperty
Definition: __HRESULT GetMethodProperty(UInt32 codecIndex, UInt64 propID, [out] PROPVARIANT \*value)__  
Description: Get specific property of selected codec  
Parameters:
|     Name     |        Type        |    Description    |
| ------------ | ------------------ | ----------------- |
|  codecIndex  | unsigned int       | Codec index       |
|  propID      | unsigned long long | Property ID       |
|  value       | PROPVARIANT \*     | Value of property |

------------

#### GetHandlerProperty
##### Currently WIP
Definition: __HRESULT GetHandlerProperty(PROPID propID, PROPVARIANT \*value)__  
Description: TBD  
Parameters:
| Name | Type | Description |
| ------------ | ------------ | ------------ |
| propID | PROPID | idk |
| value | PROPVARIANT \* | Value |

------------

#### GetHandlerProperty2
##### Currently WIP
Definition: __HRESULT GetHandlerProperty2(UInt32 formatIndex, PROPID propID, PROPVARIANT \*value)__  
Description: TBD  
Parameters:
| Name | Type | Description |
| ------------ | ------------ | ------------ |
| formatIndex | UInt32 | Format Index |
| propID | PROPID | Property ID |
| value | PROPVARIANT \* | Value |

------------

#### GetPluginProperty
Definition: __HRESULT GetPluginProperty(UInt64 propID, [out] PROPVARIANT \*value)__  
Description: Get specific plugin's property. Plugin should answer with its name, type, class id and options class id  
Parameters:
|     Name     |        Type        |    Description    |
| ------------ | ------------------ | ----------------- |
| propID       | unsigned long long | Property ID       |
| value        | PROPVARIANT \*     | Value of property |

------------

#### GetHashers
##### Currently WIP
Definition: __HRESULT GetHashers(IHashers \*\*hashers)__  
Description: TBD  
Parameters:
| Name | Type | Description |
| ------------ | ------------ | ------------ |
| hashers | IHashers ** | Hashers |

------------

#### GetIsArc
##### Currently WIP
Definition: __HRESULT GetIsArc(UInt32 formatIndex, Func_IsArc \*isArc)__  
Description: TBD  
Parameters:
| Name | Type | Description |
| ------------ | ------------ | ------------ |
| formatIndex | UInt32 | Format Index |
| isArc | Func_IsArc \* | idk |

------------

#### SetLargePageMode
Definition: __HRESULT SetLargePageMode()__  
Description: Enable Large-Page mode for this plugin   
Parameters: *NONE*

------------

#### SetCaseSensitive
Definition: __HRESULT SetCaseSensitive(Int32 caseSensitive)__  
Description: Toggle case sensitivity for paths and filenames  
Parameters:
|      Name     |     Type     |         Description        |
| ------------- | ------------ | -------------------------- |
| caseSensitive | int          | Is case sensitive (1 or 0) |

------------

#### SetCodecs
##### Currently WIP
Definition: __HRESULT SetCodecs(ICompressCodecsInfo \*compressCodecsInfo)__  
Description: TBD  
Parameters:
| Name | Type | Description |
| ------------ | ------------ | ------------ |
| compressCodecsInfo | ICompressCodecsInfo \* | idk |
