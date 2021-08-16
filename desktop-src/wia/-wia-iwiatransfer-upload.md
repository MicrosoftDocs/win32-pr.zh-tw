---
description: 從呼叫端起始單一專案的資料上傳。
ms.assetid: 301ac5d9-b864-4c3c-bd4b-143cc4032dcb
title: 'IWiaTransfer：： Upload 方法 (Wia. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransfer.Upload
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 66bd542d27f29aa8fd531b6f3d8089d296efe2d963bcf967a0c1ab07e6f0db8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118208236"
---
# <a name="iwiatransferupload-method"></a>IWiaTransfer：： Upload 方法

從呼叫端起始單一專案的資料上傳。

## <a name="syntax"></a>語法


```C++
HRESULT Upload(
  [in] LONG                 lFlags,
  [in] IStream              *pSource,
  [in] IWiaTransferCallback *pIWiaTransferCallback
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lFlags* \[在\]
</dt> <dd>

類型： **LONG**

目前未使用。 應該設定為零。

</dd> <dt>

*pSource* \[在\]
</dt> <dd>

類型： **[IStream](/windows/win32/api/objidl/nn-objidl-istream)\***

指定 [IStream](/windows/win32/api/objidl/nn-objidl-istream) 資料的指標。

</dd> <dt>

*pIWiaTransferCallback* \[在\]
</dt> <dd>

類型： **[ **IWiaTransferCallback**](-wia-iwiatransfercallback.md)\***

指定呼叫端之 [**IWiaTransferCallback**](-wia-iwiatransfercallback.md) 介面的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                   |
| 標頭<br/>                   | <dl> <dt>Wia</dt> </dl>       |
| IDL<br/>                      | <dl> <dt>Wia .idl</dt> </dl>     |
| 程式庫<br/>                  | <dl> <dt>Wiaguid .lib</dt> </dl> |



 

 
