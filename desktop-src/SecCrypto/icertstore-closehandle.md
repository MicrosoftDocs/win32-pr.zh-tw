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
ms.openlocfilehash: bb1e9ab032b76b8ef02de786d1fc39af0b0d54b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987852"
---
# <a name="icertstoreclosehandle-method"></a>ICertStore：： CloseHandle 方法

\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。\]

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

 

 




