---
title: 'INapComponentConfig SetConfig 方法 (NapCommon .h) '
description: 設定 (SHV) 元件設定的系統健全狀況驗證程式。
ms.assetid: ec27e30b-4205-40bc-a24b-61072a746e53
keywords:
- SetConfig 方法 NAP
- SetConfig 方法 NAP，INapComponentConfig 介面
- INapComponentConfig 介面 NAP，SetConfig 方法
topic_type:
- apiref
api_name:
- INapComponentConfig.SetConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7b3ecf455c591985a5e8778e49495351bd1b4aba83e9d29fe2b25d7d406a507
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940196"
---
# <a name="inapcomponentconfigsetconfig-method"></a>INapComponentConfig：： SetConfig 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**SetConfig** 方法會設定 (SHV) 元件設定的系統健全狀況驗證程式。

## <a name="syntax"></a>語法


```C++
HRESULT SetConfig(
  [in] UINT16 bCount,
  [in] BYTE   *data
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*bCount* \[在\]
</dt> <dd>

*資料* 設定 blob 的大小（以位元組為單位）。

</dd> <dt>

*資料* \[在\]
</dt> <dd>

SHV 元件設定資料的指標。

> [!Note]  
> 使用 [**GetConfig**](inapcomponentconfig-getconfig.md) 方法從 x86 電腦匯出的設定資料，可以使用 **SetConfig** 方法匯入至 x64 電腦，反之亦然。 因此，設定資料的格式必須是與架構無關的格式，例如 XML。 使用 XML 而非位元組資料流程可讓您更輕鬆地在不同的架構上使用設定資料。 設定資料中使用的 XML 元素是由實施者決定。

 

</dd> </dl>

## <a name="return-value"></a>傳回值

根據此操作的結果，傳回下列其中一個錯誤碼。



| 傳回碼                                                                                     | 描述                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> </dl>           | 作業成功。<br/>                            |
| <dl> <dt>**E \_ACCESSDENIED**</dt> </dl> | 許可權錯誤，拒絕存取。<br/>                       |
| <dl> <dt>**E \_OUTOFMEMORY**</dt> </dl>  | 系統資源限制，無法執行操作。<br/> |



 

## <a name="remarks"></a>備註

元件版本設定資訊應包含在 *資料* 設定 blob 中。 從一個 SHV 版本遷移到另一個版本時，可能會使用版本設定資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>NapCommon。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapCommon .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**INapComponentConfig**](inapcomponentconfig.md)
</dt> <dt>

[**INapConponentConfig::GetConfig**](inapcomponentconfig-getconfig.md)
</dt> </dl>

 

 





