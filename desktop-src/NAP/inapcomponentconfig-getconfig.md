---
title: 'INapComponentConfig GetConfig 方法 (NapCommon .h) '
description: 抓取 (SHV) 元件設定的系統健全狀況驗證程式。
ms.assetid: 57a1d3a7-05c0-4e0f-91b8-b3cf8982d04f
keywords:
- GetConfig 方法 NAP
- GetConfig 方法 NAP，INapComponentConfig 介面
- INapComponentConfig 介面 NAP，GetConfig 方法
topic_type:
- apiref
api_name:
- INapComponentConfig.GetConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3e07465d768c8902166150e53d4200e775e2597
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466460"
---
# <a name="inapcomponentconfiggetconfig-method"></a>INapComponentConfig：： GetConfig 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**GetConfig** 方法會 (SHV) 元件設定來抓取系統健全狀況驗證程式。

## <a name="syntax"></a>語法


```C++
HRESULT GetConfig(
  [out] UINT16 *bCount,
  [out] BYTE   **data
) const;
```



## <a name="parameters"></a>參數

<dl> <dt>

*bCount* \[擴展\]
</dt> <dd>

*資料* 設定 blob 的大小（以位元組為單位）。

</dd> <dt>

*資料* \[擴展\]
</dt> <dd>

SHV 元件設定資料的位址指標。

> [!Note]  
> 使用 **GetConfig** 方法從 x86 電腦匯出的設定資料，可以使用 [**SetConfig**](inapcomponentconfig-setconfig.md) 方法匯入至 x64 電腦，反之亦然。 因此，設定資料的格式必須是與架構無關的格式，例如 XML。 使用 XML 而非位元組資料流程可讓您更輕鬆地在不同的架構上使用設定資料。 設定資料中使用的 XML 元素是由實施者決定。

 

</dd> </dl>

## <a name="return-value"></a>傳回值

根據此操作的結果，傳回下列其中一個錯誤碼。



| 傳回碼                                                                                     | Description                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> </dl>           | 作業成功。<br/>                            |
| <dl> <dt>**E \_ACCESSDENIED**</dt> </dl> | 許可權錯誤，拒絕存取。<br/>                       |
| <dl> <dt>**E \_OUTOFMEMORY**</dt> </dl>  | 系統資源限制，無法執行操作。<br/> |



 

## <a name="remarks"></a>備註

資料參數必須由被呼叫端配置 (元件實作項) 使用 **CoTaskMemAlloc** ，並由呼叫者使用 **CoTaskMemFree** 釋放。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>NapCommon。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCommon .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**INapComponentConfig**](inapcomponentconfig.md)
</dt> <dt>

[**INapComponentConfig::SetConfig**](inapcomponentconfig-setconfig.md)
</dt> </dl>

 

 





