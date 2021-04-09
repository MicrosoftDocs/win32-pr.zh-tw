---
title: 'ResourceLocator. FragmentPath 屬性 (WSManDisp .h) '
description: 取得或設定在會話物件作業（例如 Session. Get、Session. Put 或 Session. 列舉）中使用 ResourceLocator 時，資源片段或屬性的路徑。
ms.assetid: 4d059b57-fca5-4a75-9396-6505920498c3
ms.tgt_platform: multiple
keywords:
- FragmentPath 屬性 Windows 遠端管理
- FragmentPath 屬性 Windows 遠端管理，ResourceLocator 物件
- ResourceLocator 物件 Windows 遠端管理、FragmentPath 屬性
topic_type:
- apiref
api_name:
- ResourceLocator.FragmentPath
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e15fba102f9a7c8a2581271c575857b49bc5df1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025135"
---
# <a name="resourcelocatorfragmentpath-property"></a>ResourceLocator. FragmentPath 屬性

取得或設定在 [**會話**](session.md)物件作業（例如 [**session. Get**](session-get.md)、 [**session. Put**](session-put.md)或 [**session. 列舉**](session-enumerate.md)）中使用 [**ResourceLocator**](resourcelocator.md)時，[*資源*](windows-remote-management-glossary.md)[*片段*](windows-remote-management-glossary.md)或屬性的路徑。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```VB
ResourceLocator.FragmentPath
```



## <a name="property-value"></a>屬性值

識別資源之片段或屬性的字串。 例如，如果資源是磁片磁碟機，而要求的屬性是製造商，則字串可能包含 `Diskdrive/Manufacturer` 。 片段文字會區分大小寫。 在此情況下，您不能使用 `diskdrive/manufacturer` 。

## <a name="remarks"></a>備註

**IWSManResourceLocator：： FragmentPath** 是對應的 c + + 屬性。

您可以藉由提供陣列索引來指定陣列屬性的一個元素，如下列範例所示。 請注意，陣列索引的開頭是1，而不是0。


```VB
Const Uri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_NetworkAdapterConfiguration"
Const FragmentPath = "DNSServerSearchOrder[1]"
```



若要取得整個陣列，請指定陣列屬性名稱，如下列範例所示。


```VB
Const Uri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_NetworkAdapterConfiguration"
Const FragmentPath = "DNSServerSearchOrder"
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                 |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                           |
| 標頭<br/>                   | <dl> <dt>WSManDisp。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp .idl</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>WSManDisp .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ResourceLocator**](resourcelocator.md)
</dt> </dl>

 

 





