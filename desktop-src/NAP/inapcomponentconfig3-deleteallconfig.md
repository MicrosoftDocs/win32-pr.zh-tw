---
title: 'INapComponentConfig3 DeleteAllConfig 方法 (NapCommon .h) '
description: 是由系統健康狀態驗證 (Shv 所執行) ，以提供在安裝之後將 SHV 存放區重設為其原始狀態的方法。
ms.assetid: 7f079743-1c32-430d-a250-b49a96b99f14
keywords:
- DeleteAllConfig 方法 NAP
- DeleteAllConfig 方法 NAP，INapComponentConfig3 介面
- INapComponentConfig3 介面 NAP，DeleteAllConfig 方法
topic_type:
- apiref
api_name:
- INapComponentConfig3.DeleteAllConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12a766690114db20fb9be5cccbd4508f4565f2cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843336"
---
# <a name="inapcomponentconfig3deleteallconfig-method"></a>INapComponentConfig3：:D eleteAllConfig 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**DeleteAllConfig** 方法是由系統健康狀態驗證 (shv) 來提供在安裝之後，將 SHV 存放區重設為其原始狀態的方法。 所有設定資料（預設設定除外）都必須刪除。

## <a name="syntax"></a>語法


```C++
HRESULT DeleteAllConfig();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

根據此操作的結果，傳回下列其中一個錯誤碼。



| 傳回碼                                                                           | Description                             |
|---------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**S \_確定**</dt> </dl> | 作業成功。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>NapCommon。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCommon .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**INapComponentConfig3**](inapcomponentconfig3.md)
</dt> </dl>

 

 





