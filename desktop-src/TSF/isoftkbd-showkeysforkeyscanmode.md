---
title: 'ISoftKbd ShowKeysForKeyScanMode 方法 (Softkbdc .h) '
description: ISoftKbd ShowKeysForKeyScanMode 方法會顯示軟鍵盤的金鑰掃描模式所使用的金鑰。
ms.assetid: bfa76e5b-6f6e-470a-ba3a-7ecff9f67f7b
keywords:
- ShowKeysForKeyScanMode 方法文字服務架構
- ShowKeysForKeyScanMode 方法文字服務架構，ISoftKbd 介面
- ISoftKbd 介面文字服務架構，ShowKeysForKeyScanMode 方法
topic_type:
- apiref
api_name:
- ISoftKbd.ShowKeysForKeyScanMode
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7c46fbfc103c0ba40294e4c149d5fd427296765
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466300"
---
# <a name="isoftkbdshowkeysforkeyscanmode-method"></a>ISoftKbd：： ShowKeysForKeyScanMode 方法

**ISoftKbd：： ShowKeysForKeyScanMode** 方法會顯示軟鍵盤的金鑰掃描模式所使用的金鑰。

## <a name="syntax"></a>語法


```C++
HRESULT ShowKeysForKeyScanMode(
  [in] KEYID *lpKeyID,
  [in] INT   iKeyNum,
  [in] BOOL  fHighL
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lpKeyID* \[在\]
</dt> <dd>

KEYID 元素陣列的指標，指出要顯示之索引鍵的識別碼。

</dd> <dt>

*iKeyNum* \[在\]
</dt> <dd>

要顯示的索引鍵數目。

</dd> <dt>

*fHighL* \[在\]
</dt> <dd>

如果方法是反白顯示索引鍵，則為 TRUE，否則為 **FALSE** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 值                                                                                        | 描述                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>         | 此方法成功。<br/>        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | 其中一個參數無效。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                             |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                   |
| 可轉散發套件<br/>          | Windows 2000 Professional 上的 TSF 1。0<br/>                                        |
| 標頭<br/>                   | <dl> <dt>Softkbdc。h</dt> </dl>  |
| Idl<br/>                      | <dl> <dt>Softkbd .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Softkbd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ISoftKbd**](isoftkbd.md)
</dt> </dl>

 

 





