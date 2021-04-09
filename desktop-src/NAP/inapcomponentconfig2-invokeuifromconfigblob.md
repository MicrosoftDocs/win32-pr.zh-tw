---
title: 'INapComponentConfig2 InvokeUIFromConfigBlob 方法 (NapCommon .h) '
description: 是由系統健康狀態驗證 (Shv) 視需要在記憶體中載入遠端或本機電腦的設定，並顯示允許操作設定資料的 UI。
ms.assetid: 9c012690-6751-4a47-8683-74abac610c77
keywords:
- InvokeUIFromConfigBlob 方法 NAP
- InvokeUIFromConfigBlob 方法 NAP，INapComponentConfig2 介面
- INapComponentConfig2 介面 NAP，InvokeUIFromConfigBlob 方法
topic_type:
- apiref
api_name:
- INapComponentConfig2.InvokeUIFromConfigBlob
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54cc1efaf7da3434e1aff10d57c2e175481a3d2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843339"
---
# <a name="inapcomponentconfig2invokeuifromconfigblob-method"></a>INapComponentConfig2：： InvokeUIFromConfigBlob 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**InvokeUIFromConfigBlob** 方法是由系統健康狀態驗證 (shv) 視需要在記憶體中載入遠端或本機電腦的設定，並顯示允許操作設定資料的 UI。 Configuration 元件必須支援透過 DCOM 使用 [**INapComponentConfig**](inapcomponentconfig.md) 。

## <a name="syntax"></a>語法


```C++
HRESULT InvokeUIFromConfigBlob(
  [in, unique] HWND   hwndParent,
  [in]         UINT16 inbCount,
  [in]         BYTE   *inData,
  [out]        UINT16 *outbCount,
  [out]        BYTE   **outdata,
  [out]        BOOL   *fConfigChanged
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hwndParent* \[在\]
</dt> <dd>

父系或擁有者視窗的控制碼。 必須提供有效的視窗控制碼。

</dd> <dt>

*inbCount* \[在\]
</dt> <dd>

*InData* 的大小（以位元組為單位）。

</dd> <dt>

*inData* \[在\]
</dt> <dd>

儲存初始設定資料之緩衝區的指標。 這項資料會從遠端或本機電腦匯出。

</dd> <dt>

*outbCount* \[擴展\]
</dt> <dd>

*Outdata* 的大小（以位元組為單位）。

</dd> <dt>

*outdata* \[擴展\]
</dt> <dd>

緩衝區的指標，此緩衝區會儲存由 SHV 設定使用者介面變更的設定資料。 這項資料是由遠端或本機電腦匯入。

</dd> <dt>

*fConfigChanged* \[擴展\]
</dt> <dd>

**布林** 值的指標，如果在 UI 作業期間變更設定，則設定為 **TRUE** ，否則為 **FALSE** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_如果成功或其中一個標準 Windows 錯誤碼，則會傳回 S OK。

## <a name="remarks"></a>備註

如果用於本機電腦，則此函式可用於每個原則 SHV 設定。 它提供一種方法來叫用 SHV UI 和編輯現有的 SHV 設定。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>NapCommon。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCommon .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**INapComponentConfig2**](inapcomponentconfig2.md)
</dt> </dl>

 

 





