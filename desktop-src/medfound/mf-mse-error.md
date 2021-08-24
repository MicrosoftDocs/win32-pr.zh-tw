---
description: 定義媒體來源延伸模組的不同錯誤狀態。
ms.assetid: 8FD54833-F60B-49E8-A673-6130F3B06160
title: MF_MSE_ERROR 列舉
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_MSE_ERROR
api_type:
- HeaderDef
api_location:
- mfmediaengine.h
ms.openlocfilehash: 71246aaa2897540b272360a790718f8d5900934108c98dfcc6b4023898f9f2db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104584"
---
# <a name="mf_mse_error-enumeration"></a>MF \_ MSE \_ 錯誤列舉

定義媒體來源延伸模組的不同錯誤狀態。

## <a name="syntax"></a>Syntax


```C++
typedef enum _MF_MSE_ERROR { 
  MF_MSE_ERROR_NOERROR        =  0,
  MF_MSE_ERROR_NETWORK        = 1,
  MF_MSE_ERROR_DECODE         = 2,
  MF_MSE_ERROR_UNKNOWN_ERROR  =  3
} MF_MSE_ERROR;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="MF_MSE_ERROR_NOERROR"></span><span id="mf_mse_error_noerror"></span>**MF \_ MSE \_ 錯誤 \_ >AAD-USERREADUSINGALTERNATIVESECURITYID-NOERROR**
</dt> <dd>

未指定錯誤。

</dd> <dt>

<span id="MF_MSE_ERROR_NETWORK"></span><span id="mf_mse_error_network"></span>**MF \_ MSE \_ 錯誤 \_ 網路**
</dt> <dd>

指定網路發生錯誤。

</dd> <dt>

<span id="MF_MSE_ERROR_DECODE"></span><span id="mf_mse_error_decode"></span>**MF \_ MSE \_ 錯誤 \_ 解碼**
</dt> <dd>

指定解碼時發生錯誤。

</dd> <dt>

<span id="MF_MSE_ERROR_UNKNOWN_ERROR"></span><span id="mf_mse_error_unknown_error"></span>**MF \_ MSE \_ 錯誤 \_ 不明 \_ 錯誤**
</dt> <dd>

指定未知的錯誤。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1 \[僅限桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | Windows Server 2012\[僅限 R2 desktop 應用程式\]<br/>                                      |
| IDL<br/>                      | <dl> <dt>Mfmediaengine .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎列舉](media-foundation-enumerations.md)
</dt> </dl>

 

 




