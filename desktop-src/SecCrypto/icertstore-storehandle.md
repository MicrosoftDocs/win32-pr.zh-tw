---
description: 設定或抓取證書存儲的 HCERTSTORE 控制碼。
ms.assetid: 3ff8b4c7-4a9a-4cc1-b0ea-da442ebce157
title: ICertStore：： StoreHandle 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertStore.StoreHandle
- ICertStore.get_StoreHandle
- ICertStore.put_StoreHandle
- CertStore.StoreHandle
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2858e7484c82663b2ba6866d0f17b5528921619dbfa80cbb76ec0eabbb39a332
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005616"
---
# <a name="icertstorestorehandle-property"></a>ICertStore：： StoreHandle 屬性

\[CAPICOM 是僅限32位的元件，可供下列作業系統使用： Windows Server 2008、Windows Vista 和 Windows XP。\]

**StoreHandle** 屬性會設定或抓取證書存儲的 HCERTSTORE 控制碼。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```VB
CertStore.StoreHandle As Long
```



## <a name="property-value"></a>屬性值

憑證存放區的 HCERTSTORE 控制碼。

## <a name="error-codes"></a>錯誤碼

如果屬性存取方法 **put \_ StoreHandle** 並 **讓 \_ StoreHandle** 成功，則會傳回 S \_ OK。

任何其他 **HRESULT** 值都表示呼叫失敗。

## <a name="remarks"></a>備註

您必須呼叫 [**CloseHandle**](icertstore-closehandle.md) 方法或 [**CertCloseStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore) 函數來釋放內容。

如果您設定 **StoreHandle** 屬性，則會重設整個 [**存放區**](store.md) 物件的狀態。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ICertStore**](icertstore.md)
</dt> </dl>

 

 




