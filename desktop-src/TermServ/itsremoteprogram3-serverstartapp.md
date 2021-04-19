---
title: ITSRemoteProgram3 ServerStartApp 方法
description: 指定要在遠端會話中啟動的應用程式。
ms.assetid: 55a05d05-66d5-48a1-b3a6-f087aeb62925
ms.tgt_platform: multiple
keywords:
- ServerStartApp 方法遠端桌面服務
- ServerStartApp 方法遠端桌面服務，ITSRemoteProgram3 介面
- ITSRemoteProgram3 介面遠端桌面服務，ServerStartApp 方法
topic_type:
- apiref
api_name:
- ITSRemoteProgram3.ServerStartApp
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef1822fa98094870ebebe607528cdc69a8a201f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106970450"
---
# <a name="itsremoteprogram3serverstartapp-method"></a>ITSRemoteProgram3：： ServerStartApp 方法

指定要在遠端會話中啟動的應用程式。

## <a name="syntax"></a>語法


```C++
HRESULT ServerStartApp(
  [in] BSTR         bstrAppUserModelId,
  [in] BSTR         bstrArguments,
  [in] VARIANT_BOOL vbExpandEnvVarInArgumentsOnServer
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*bstrAppUserModelId* \[在\]
</dt> <dd></dd> <dt>

*bstrArguments* \[在\]
</dt> <dd></dd> <dt>

*vbExpandEnvVarInArgumentsOnServer* \[在\]
</dt> <dd></dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 10 桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | Windows Server 2016<br/>                                                         |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITSRemoteProgram3**](itsremoteprogram3.md)
</dt> </dl>

 

 





