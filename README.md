## 7zip Plugin Development Kit
7zipPDK allow you to write and compile external codecs and formats for 7zip in c++

### Full Exports List
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
#### STDAPI CreateObject(const GUID \*clsid, const GUID \*iid, void \*\*outObject)
Description: Idk  
Return: Error code  
Parameters:
| Name | Type | Description |
| ------------ | ------------ | ------------ |
| clsid | GUID \* | Your id? |
| iid | GUID \* | idk |
| outObject | void ** | Some memory |

------------

#### STDAPI CreateDecoder(UInt32 index, const GUID \*iid, void \*\*outObject)
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
Description: Idk  
Return: Error code  
Parameters:
| Name | Type | Description |
| ------------ | ------------ | ------------ |
| index | UInt32 | Encoder id? |
| iid | GUID \* | idk |
| outObject | void ** | Some memory |

------------

#### STDAPI GetNumberOfMethods(UINT32 \*numCodecs)
Description: Idk  
Return: Error code  
Parameters:
| Name | Type | Description |
| ------------ | ------------ | ------------ |
| numCodecs | UINT32 \* | Return value |

------------

#### STDAPI GetNumberOfFormats(UINT32 \*numFormats)
Description: Idk  
Return: Error code  
Parameters:
| Name | Type | Description |
| ------------ | ------------ | ------------ |
| numFormats | UINT32 \* | Return value |

------------

#### STDAPI GetMethodProperty(UInt32 codecIndex, PROPID propID, PROPVARIANT \*value)
Description: Idk  
Return: Error code  
Parameters:
| Name | Type | Description |
| ------------ | ------------ | ------------ |
| codecIndex | UInt32 | Codec Index |
| propID | PROPID | Property ID |
| value | PROPVARIANT \* | Value |

------------

#### STDAPI GetHandlerProperty(PROPID propID, PROPVARIANT \*value)
Description: Idk  
Return: Error code  
Parameters:
| Name | Type | Description |
| ------------ | ------------ | ------------ |
| propID | PROPID | idk |
| value | PROPVARIANT \* | Value |

------------

#### STDAPI GetHandlerProperty2(UInt32 formatIndex, PROPID propID, PROPVARIANT \*value)
Description: Idk  
Return: Error code  
Parameters:
| Name | Type | Description |
| ------------ | ------------ | ------------ |
| formatIndex | UInt32 | Format Index |
| propID | PROPID | Property ID |
| value | PROPVARIANT \* | Value |

------------

#### STDAPI GetPluginProperty(PROPID propID, PROPVARIANT \*value)
Description: Idk  
Return: Error code  
Parameters:
| Name | Type | Description |
| ------------ | ------------ | ------------ |
| propID | PROPID | Property ID |
| value | PROPVARIANT \* | Value |

------------

#### STDAPI GetHashers(IHashers \*\*hashers)
Description: Idk  
Return: Error code  
Parameters:
| Name | Type | Description |
| ------------ | ------------ | ------------ |
| hashers | IHashers ** | Hashers |

------------

#### STDAPI GetIsArc(UInt32 formatIndex, Func_IsArc \*isArc)
Description: Idk  
Return: Error code  
Parameters:
| Name | Type | Description |
| ------------ | ------------ | ------------ |
| formatIndex | UInt32 | Format Index |
| isArc | Func_IsArc \* | idk |

------------

#### STDAPI SetLargePageMode()
Description: Update Large Page Mode and its size  
Return: Error code  
Parameters: *NONE*

------------

#### STDAPI SetCaseSensitive(Int32 caseSensitive)
Description: Set case sensitivity for path and filenames  
Return: Error code  
Parameters:
| Name | Type | Description |
| ------------ | ------------ | ------------ |
| caseSensitive | Int32 | Is case sensitive (1 or 0) |

------------

#### STDAPI SetCodecs(ICompressCodecsInfo \*compressCodecsInfo)
Description: Idk  
Return: Error code  
Parameters:
| Name | Type | Description |
| ------------ | ------------ | ------------ |
| compressCodecsInfo | ICompressCodecsInfo \* | idk |
