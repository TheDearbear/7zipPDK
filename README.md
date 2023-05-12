## 7zip Plugin Development Kit
7zipPDK allow you to write and compile external codecs and formats for 7zip in c++

### Full Exports List
 - CreateObject
 - CreateDecoder
 - CreateEncoder
 - [GetNumberOfMethods](#hresult-getnumberofmethodsuint32-numcodecs)
 - [GetNumberOfFormats](#hresult-getnumberofformatsuint32-numformats)
 - [GetMethodProperty](#hresult-getmethodpropertyuint32-codecindex-uint64-propid-propvariant-value)
 - GetHandlerProperty
 - GetHandlerProperty2
 - [GetPluginProperty](#hresult-getpluginpropertyuint64-propid-propvariant-value)
 - GetHashers
 - GetIsArc
 - [SetLargePageMode](#hresult-setlargepagemode)
 - [SetCaseSensitive](#hresult-setcasesensitiveint32-casesensitive)
 - SetCodecs

### Exports Overview
#### STDAPI CreateObject(const GUID \*clsid, const GUID \*iid, void \*\*outObject)
##### Currently WIP
Description: This function will be called if 7zip need to create codec, hasher, archiver or any other stuff  
Return: Int32 | Error code  
Parameters:
| Name | Type | Description |
| ------------ | ------------ | ------------ |
| clsid | GUID \* | Requested class |
| iid | GUID \* | Requested category |
| outObject | void \*\* | Function result |

------------

#### STDAPI CreateDecoder(UInt32 index, const GUID \*iid, void \*\*outObject)
##### Currently WIP
Description: Idk  
Return: Error code  
Parameters:
| Name | Type | Description |
| ------------ | ------------ | ------------ |
| index | UInt32 | Decoder id? |
| iid | GUID \* | idk |
| outObject | void ** | Some memory |

------------

#### STDAPI CreateEncoder(UInt32 index, const GUID \*iid, void \*\*outObject)
##### Currently WIP
Description: Idk  
Return: Error code  
Parameters:
| Name | Type | Description |
| ------------ | ------------ | ------------ |
| index | UInt32 | Encoder id? |
| iid | GUID \* | idk |
| outObject | void ** | Some memory |

------------

#### HRESULT GetNumberOfMethods(UInt32 \*numCodecs)
Description: Get number of supported codecs by this plugin  
Return: Error code  
Parameters:
|     Name     |      Type       |   Description    |
| ------------ | --------------- | ---------------- |
|   numCodecs  | unsigned int \* | Number of codecs |

------------

#### HRESULT GetNumberOfFormats(UInt32 \*numFormats)
Description: Get number of supported formats by this plugin  
Return: Error code  
Parameters:
|     Name     |       Type      |    Description    |
| ------------ | --------------- | ----------------- |
|  numFormats  | unsigned int \* | Number of formats |

------------

#### HRESULT GetMethodProperty(UInt32 codecIndex, UInt64 propID, PROPVARIANT \*value)
Description: Get specific property of selected codec  
Return: Error code  
Parameters:
|     Name     |        Type        |    Description    |
| ------------ | ------------------ | ----------------- |
|  codecIndex  | unsigned int       | Codec index       |
|  propID      | unsigned long long | Property ID       |
|  value       | PROPVARIANT \*     | Value of property |

------------

#### STDAPI GetHandlerProperty(PROPID propID, PROPVARIANT \*value)
##### Currently WIP
Description: Idk  
Return: Error code  
Parameters:
| Name | Type | Description |
| ------------ | ------------ | ------------ |
| propID | PROPID | idk |
| value | PROPVARIANT \* | Value |

------------

#### STDAPI GetHandlerProperty2(UInt32 formatIndex, PROPID propID, PROPVARIANT \*value)
##### Currently WIP
Description: Idk  
Return: Error code  
Parameters:
| Name | Type | Description |
| ------------ | ------------ | ------------ |
| formatIndex | UInt32 | Format Index |
| propID | PROPID | Property ID |
| value | PROPVARIANT \* | Value |

------------

#### HRESULT GetPluginProperty(UInt64 propID, PROPVARIANT \*value)
Description: Get specific plugin's property. Plugin should answer with its name, type, class id and options class id  
Return: Error code  
Parameters:
|     Name     |        Type        |    Description    |
| ------------ | ------------------ | ----------------- |
| propID       | unsigned long long | Property ID       |
| value        | PROPVARIANT \*     | Value of property |

------------

#### STDAPI GetHashers(IHashers \*\*hashers)
##### Currently WIP
Description: Idk  
Return: Error code  
Parameters:
| Name | Type | Description |
| ------------ | ------------ | ------------ |
| hashers | IHashers ** | Hashers |

------------

#### STDAPI GetIsArc(UInt32 formatIndex, Func_IsArc \*isArc)
##### Currently WIP
Description: Idk  
Return: Error code  
Parameters:
| Name | Type | Description |
| ------------ | ------------ | ------------ |
| formatIndex | UInt32 | Format Index |
| isArc | Func_IsArc \* | idk |

------------

#### HRESULT SetLargePageMode()
Description: Enable Large-Page mode for this plugin  
Return: Error code  
Parameters: *NONE*

------------

#### HRESULT SetCaseSensitive(Int32 caseSensitive)
Description: Toggle case sensitivity for paths and filenames  
Return: Error code  
Parameters:
|      Name     |     Type     |         Description        |
| ------------- | ------------ | -------------------------- |
| caseSensitive | int          | Is case sensitive (1 or 0) |

------------

#### STDAPI SetCodecs(ICompressCodecsInfo \*compressCodecsInfo)
##### Currently WIP
Description: Idk  
Return: Error code  
Parameters:
| Name | Type | Description |
| ------------ | ------------ | ------------ |
| compressCodecsInfo | ICompressCodecsInfo \* | idk |
