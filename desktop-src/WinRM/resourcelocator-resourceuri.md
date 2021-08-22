---
title: 'ResourceLocator 屬性 (WSManDisp .h) '
description: 取得或設定 ResourceLocator 物件中的資源 URI。
ms.assetid: adb1e08a-290f-4a23-a6e4-d7567a6b7eee
ms.tgt_platform: multiple
keywords:
- ResourceURI 屬性 Windows 遠端管理
- ResourceURI 屬性 Windows 遠端管理，ResourceLocator 物件
- ResourceLocator 物件 Windows 遠端管理，ResourceURI 屬性
topic_type:
- apiref
api_name:
- ResourceLocator.ResourceURI
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 323240462dad32ba757897798b663b78b373ebb3ab3e60c3387dd7da8eef4c85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642858"
---
# <a name="resourcelocatorresourceuri-property"></a>ResourceLocator 屬性

取得或設定 [**ResourceLocator**](resourcelocator.md)物件中的 [*資源 URI*](windows-remote-management-glossary.md) 。 您可以提供 [**ResourceLocator**](resourcelocator.md) 物件，而不是在 [**會話**](session.md) 物件作業中指定資源 URI，例如 [**session. Get**](session-get.md)、 [**session. Put**](session-put.md)或 [**Session。列舉**](session-enumerate.md)。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```VB
ResourceLocator.ResourceURI As string
```



## <a name="property-value"></a>屬性值

識別資源的字串。 設定 [**ResourceLocator**](resourcelocator.md) 物件的資源 URI 時，URI 必須只包含路徑。

## <a name="remarks"></a>備註

以下是適用于 [**ResourceURI**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanresourcelocator-get_resourceuri)的適當路徑範例。

``` syntax
"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service"
```

下列路徑無法運作，因為它包含特定實例的索引鍵。 使用 [**ResourceLocator. AddSelector**](resourcelocator-addselector.md) 方法來指定特定的實例。

``` syntax
"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"
```

**IWSManResourceLocator：： ResourceURI** 是對應的 c + + 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                 |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                           |
| 標頭<br/>                   | <dl> <dt>WSManDisp。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp .idl</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>WSManDisp .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ResourceLocator**](resourcelocator.md)
</dt> </dl>

 

 





