---
description: 設定或抓取 \_ 憑證存放區的 CAPICOM 存放區 \_ 位置。
ms.assetid: 2bb76f51-f092-4dbe-93e9-1fdc185c7c50
title: ICertStore：： StoreLocation 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertStore.StoreLocation
- ICertStore.get_StoreLocation
- ICertStore.put_StoreLocation
- CertStore.StoreLocation
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ea11da4fc908a2a3b665b2491614dbffeaa3034a3127617c562c3365522df835
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005606"
---
# <a name="icertstorestorelocation-property"></a>ICertStore：： StoreLocation 屬性

\[CAPICOM 是僅限32位的元件，可供下列作業系統使用： Windows Server 2008、Windows Vista 和 Windows XP。\]

**StoreLocation** 屬性會設定或抓取證書存儲的 [**CAPICOM \_ 存放區 \_ 位置**](capicom-store-location.md)。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```VB
CertStore.StoreLocation As CAPICOM_STORE_LOCATION
```



## <a name="property-value"></a>屬性值

憑證存放區的位置。

## <a name="error-codes"></a>錯誤碼

如果屬性存取方法 **put \_ StoreLocation** 並 **讓 \_ StoreLocation** 成功，則會傳回 S \_ OK。

任何其他 **HRESULT** 值都表示呼叫失敗。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ICertStore**](icertstore.md)
</dt> </dl>

 

 




