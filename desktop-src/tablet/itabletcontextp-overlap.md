---
description: 將 tablet 內容移至輸入佇列的前端或背面。
ms.assetid: ef4521b5-776b-46dc-864a-625bc221054a
title: ITabletCoNtextP：：重迭方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletContextP.Overlap
api_type:
- COM
api_location:
- Wisptis.exe
- Wisptis.exe.dll
ms.openlocfilehash: b009bc08dddb15bc7aa5b12c8846ea66c4a52e56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990404"
---
# <a name="itabletcontextpoverlap-method"></a>ITabletCoNtextP：：重迭方法

將 tablet 內容移至輸入佇列的前端或背面。

## <a name="syntax"></a>語法


```C++
HRESULT Overlap(
  [in]  BOOL  bTop,
  [out] DWORD *pdwtcid
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*bTop* \[在\]
</dt> <dd>

表示 tablet 內容是否應該移至輸入佇列的頂端或底部。

</dd> <dt>

*pdwtcid* \[擴展\]
</dt> <dd>

Tablet 內容識別碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                            | Description                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>   | 成功。<br/>                       |
| <dl> <dt>**E \_ 失敗**</dt> </dl> | 發生未指定的錯誤。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                              |
| 程式庫<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITabletCoNtextP 介面**](itabletcontextp.md)
</dt> </dl>

 

 




