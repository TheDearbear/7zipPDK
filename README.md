## 7zip Plugin Development Kit
7zipPDK allow you to write and compile external codecs and formats for 7zip in c++

### Full Exports List
Unused (commented out):
 - LibStartup
 - MAPISendDocuments (Mapi32.dll only)
 - DwmGetWindowAttribute

Mapi32.dll exclusive:
 - MAPISendDocuments
 - MAPISendMail

Available:
 - CreateObject
 - CreateDecoder
 - CreateEncoder
 - GetNumberOfMethods
 - GetNumberOfFormats
 - GetMethodProperty
 - GetHandlerProperty
 - GetHandlerProperty2
 - GetPluginProperty
 - GetHashers
 - GetIsArc
 - SetLargePageMode
 - SetCaseSensitive
 - SetCodecs

### Exports Overview
#### STDAPI CreateObject(const GUID \*clsid, const GUID \*iid, void **outObject)
Description: Idk  
Return: Idk  
Parameters:
| Name | Type | Description |
| ------------ | ------------ | ------------ |
| clsid | GUID \* | Your id? |
| iid | GUID \* | idk |
| outObject | void ** | Some memory |

------------

#### STDAPI CreateDecoder(UInt32 index, const GUID \*iid, void **outObject)
Description: Idk  
Return: Idk  
Parameters:
| Name | Type | Description |
| ------------ | ------------ | ------------ |
| index | UInt32 | Decoder id? |
| iid | GUID \* | idk |
| outObject | void ** | Some memory |

------------

#### STDAPI CreateEncoder(UInt32 index, const GUID \*iid, void **outObject)
Description: Idk  
Return: Idk  
Parameters:
| Name | Type | Description |
| ------------ | ------------ | ------------ |
| index | UInt32 | Encoder id? |
| iid | GUID \* | idk |
| outObject | void ** | Some memory |

------------

#### STDAPI GetNumberOfMethods(UINT32 \*numCodecs)
Description: Idk  
Return: Idk  
Parameters:
| Name | Type | Description |
| ------------ | ------------ | ------------ |
| numCodecs | UINT32 \* | Return value |

------------

#### STDAPI GetNumberOfFormats(UINT32 \*numFormats)
Description: Idk  
Return: Idk  
Parameters:
| Name | Type | Description |
| ------------ | ------------ | ------------ |
| numFormats | UINT32 \* | Return value |

------------

#### STDAPI GetMethodProperty(UInt32 codecIndex, PROPID propID, PROPVARIANT \*value)
Description: Idk  
Return: Idk  
Parameters:
| Name | Type | Description |
| ------------ | ------------ | ------------ |
| codecIndex | UInt32 | Codec Index |
| propID | PROPID | Property ID |
| value | PROPVARIANT \* | Value |

------------

#### HRESULT LibStartup()
NOT USED BY PRECOMPILED 7ZIP! TO ENABLE THIS, YOU NEED TO UNCOMMENT SPECIFIC CODE AND COMPILE IT YOURSELF!  
Description: Will be called on library startup  
Return: Error code  
Parameters: *NONE*
