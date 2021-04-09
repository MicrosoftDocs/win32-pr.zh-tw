---
description: 專家必須實行 Run 函數。 網路監視器會呼叫 Run 函式來啟動專家 DLL 內的專家。
ms.assetid: 9ef3941b-d9e9-4acb-97ed-5f39573f2946
title: " (Netmon) 執行回呼函數"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Run
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: c2dff2cf70a6d989928f17447fa3491dd9509f24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848181"
---
# <a name="run-callback-function"></a>執行回呼函數

專家必須實行 **Run** 函數。 網路監視器會呼叫 **Run** 函式來啟動專家 DLL 內的專家。

## <a name="syntax"></a>語法


```C++
BOOL WINAPI Run(
  _In_ HEXPERTKEY         hExpertKey,
  _In_ PEXPERTCONFIG      pConfig,
  _In_ PEXPERTSTARTUPINFO pExpertStartupInfo,
  _In_ DWORD              StartupFlags,
  _In_ HWND               hWndParent
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hExpertKey* \[在\]
</dt> <dd>

傳遞給所有專家特定網路監視器函式之專家的唯一識別碼。

> [!Note]  
> *HExpertKey* 識別碼可能會傳遞與 [**設定**](configure.md)函數所傳遞的專家金鑰不同的專家金鑰。

 

</dd> <dt>

*>-pconfig* \[在\]
</dt> <dd>

現有設定的指標。 *>-pconfig* 參數可以是 **Null** ，這表示專家可以使用硬式編碼的預設值或 *pExpertStartupInfo* 參數所參考的啟動資訊來執行。

</dd> <dt>

*pExpertStartupInfo* \[在\]
</dt> <dd>

當專家開始時，具有焦點的 capture 元素指標。

</dd> <dt>

*StartupFlags* \[在\]
</dt> <dd>

有關專家應該如何使用 *pExpertStartupInfo* 參數的指標。

唯一定義的旗標為：



| 值                                                                                                                                                                                                                                                                                           | 意義                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EXPERT_STARTUP_FLAG_USE_STARTUP_DATA_OVER_CONFIG_DATA."></span><span id="expert_startup_flag_use_startup_data_over_config_data."></span><dl> <dt>**專家 \_ 啟動 \_ 旗標會在設定 \_ \_ \_ 資料上使用啟動資料 \_ \_ \_ 。**</dt> </dl> | 此旗標表示專家使用 *pExpertStartupInfo* 參數，且不會使用 *>-pconfig* 參數。 一般來說，當專家可以從滑鼠右鍵按一下來開始時，您可以設定這個旗標。 如果未設定旗標，則可能會發生下列兩種情況：專家不是以滑鼠右鍵按一下來啟動，也可能是由使用者以滑鼠右鍵按一下，然後由使用者進行設定。<br/> |



 

</dd> <dt>

*hWndParent* \[在\]
</dt> <dd>

父 (的 *hWnd* 參數通常是網路監視器使用者介面) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功 (也就是，如果專家從) 開始，則傳回值為 **TRUE**。

如果函式不成功，則傳回值為 **FALSE**。

## <a name="remarks"></a>備註

當執行時，專家會在 capture 檔案的框架中執行迴圈，並產生報表或建立顯示問題的事件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



 

 




