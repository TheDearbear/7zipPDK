## 7zip Plugin Development Kit
7zipPDK allow you to write and compile external codecs and formats for 7zip in c++

### Full Exports List
 - CreateObject
 - CreateDecoder
 - CreateEncoder
 - [GetNumberOfMethods](#extern-c-hresult-getnumberofmethodsunsigned-int-numcodecs)
 - [GetNumberOfFormats](#extern-c-hresult-getnumberofformatsunsigned-int-numformats)
 - [GetMethodProperty](#extern-c-hresult-getmethodpropertyunsigned-int-codecindex-unsigned-long-long-propid-propvariant-value)
 - GetHandlerProperty
 - GetHandlerProperty2
 - [GetPluginProperty](#extern-c-hresult-getpluginpropertyunsigned-long-long-propid-propvariant-value)
 - GetHashers
 - GetIsArc
 - [SetLargePageMode](#extern-c-hresult-setlargepagemode)
 - [SetCaseSensitive](#extern-c-hresult-setcasesensitiveint-casesensitive)
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

#### extern "C" HRESULT GetNumberOfMethods(unsigned int \*numCodecs)
Description: Get number of supported codecs by this plugin  
Return: Error code  
Parameters:
|     Name     |      Type       |   Description    |
| ------------ | --------------- | ---------------- |
|   numCodecs  | unsigned int \* | Number of codecs |

------------

#### extern "C" HRESULT GetNumberOfFormats(unsigned int \*numFormats)
Description: Get number of supported formats by this plugin  
Return: Error code  
Parameters:
|     Name     |       Type      |    Description    |
| ------------ | --------------- | ----------------- |
|  numFormats  | unsigned int \* | Number of formats |

------------

#### extern "C" HRESULT GetMethodProperty(unsigned int codecIndex, unsigned long long propID, PROPVARIANT \*value)
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

#### extern "C" HRESULT GetPluginProperty(unsigned long long propID, PROPVARIANT \*value)
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

#### extern "C" HRESULT SetLargePageMode()
Description: Enable Large-Page mode for this plugin
Return: Error code  
Parameters: *NONE*

------------

#### extern "C" HRESULT SetCaseSensitive(int caseSensitive)
Description: Toggle case sensitivity for pathes and filenames  
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
