---
description: 關閉透過 StoreHandle 屬性取得的 HCERTSTORE 控制碼。
ms.assetid: 1b0d3d9b-09e0-4035-88ac-2887b3ab60c9
title: ICertStore：： CloseHandle 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertStore.CloseHandle
- CertStore.CloseHandle
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3d6f1b0b44cd0fdc71f8f3d37fa9bd8290c5d606eea1f97f5bf6644f9ce8e2a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005656"
---
# <a name="icertstoreclosehandle-method"></a>ICertStore：： CloseHandle 方法

\[CAPICOM 是僅限32位的元件，可供下列作業系統使用： Windows Server 2008、Windows Vista 和 Windows XP。\]

**CloseHandle** 方法會關閉透過 [**StoreHandle**](icertstore-storehandle.md)屬性取得的 HCERTSTORE 控制碼。

## <a name="syntax"></a>語法


```VB
CertStore.CloseHandle( _
  ByVal hCertStore _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*hCertStore* \[在\]
</dt> <dd>

要關閉的 HCERTSTORE 控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是 **HRESULT**。 S 的值 **表示 \_** 成功。 任何其他值則表示作業失敗。

## <a name="remarks"></a>備註

這個方法不會釋放 [**存放區**](store.md) 物件內所包含的 HCERTSTORE 控制碼。 它只能用來釋放透過 [**StoreHandle**](icertstore-storehandle.md) 屬性取得的 HCERTSTORE 控制碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ICertStore**](icertstore.md)
</dt> </dl>

 

 




