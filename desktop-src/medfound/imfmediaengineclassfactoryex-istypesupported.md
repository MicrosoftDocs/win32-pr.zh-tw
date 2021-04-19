---
description: 取得值，這個值會指出指定的金鑰系統是否支援指定的媒體類型。
ms.assetid: 6f4f50db-e491-46c2-a8b2-1b8e51033b5b
title: IMFMediaEngineClassFactoryEx：： IsTypeSupported 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaEngineClassFactoryEx.IsTypeSupported
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 92bf3d64d36c043e9e33b897294ff74a3fda0445
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106981923"
---
# <a name="imfmediaengineclassfactoryexistypesupported-method"></a>IMFMediaEngineClassFactoryEx：： IsTypeSupported 方法

取得值，這個值會指出指定的金鑰系統是否支援指定的媒體類型。

## <a name="syntax"></a>語法


```C++
HRESULT IsTypeSupported(
   BSTR type,
   BSTR keySystem,
   BOOL *isSupported
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*type* 
</dt> <dd>

要檢查支援的 MIME 類型。

</dd> <dt>

*keySystem* 
</dt> <dd>

檢查支援的關鍵系統。

</dd> <dt>

*isSupported* 
</dt> <dd>

如果 *keySystem* 支援型別，則 **為 true** ;否則 **為 false。**

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8.1 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 R2 \[ desktop 應用程式\]<br/>                                      |
| Idl<br/>                      | <dl> <dt>Mfmediaengine .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMFMediaEngineClassFactoryEx**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineclassfactoryex)
</dt> </dl>

 

 




