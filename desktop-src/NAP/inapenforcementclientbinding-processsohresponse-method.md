---
title: 'INapEnforcementClientBinding ProcessSoHResponse 方法 (NapEnforcementClient .h) '
description: 會在強制用戶端從強制服務器收到 SoHResponse 資料 blob 時，用來處理 SoHResponse。
ms.assetid: 6ff6d2c5-9ebe-4d8c-aa27-03147e2e1122
keywords:
- ProcessSoHResponse 方法 NAP
- ProcessSoHResponse 方法 NAP，INapEnforcementClientBinding 介面
- INapEnforcementClientBinding 介面 NAP，ProcessSoHResponse 方法
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.ProcessSoHResponse
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cffd2caeaf3a39bd5c28b4850fc560dc9567a3552aad88929581efd2729acce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118621707"
---
# <a name="inapenforcementclientbindingprocesssohresponse-method"></a>INapEnforcementClientBinding：:P rocessSoHResponse 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapEnforcementClientBinding：:P rocesssohresponse** 方法可供強制用戶端在每次從強制服務器收到 SoHResponse 資料 blob 時處理 SoHResponse。

## <a name="syntax"></a>語法


```C++
HRESULT ProcessSoHResponse(
  [in] INapEnforcementClientConnection *connection
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*連接* \[在\]
</dt> <dd>

用戶端連接之 [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) 介面的 COM 指標。 在這個方法呼叫完成之後，NapAgent 不會保留與這個介面相關聯之物件的參考。

您必須使用先前建立的連接來處理 SOHResponse 資料 blob。

</dd> </dl>

## <a name="return-value"></a>傳回值

也可能傳回其他 COM 特定的錯誤碼。



| 傳回碼                                                                                             | 描述                                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> </dl>                   | 作業成功。<br/>                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>            | 先前未在強制用戶端上建立任何連接。 <br/>                                                                                                                                                                                                                                                 |
| <dl> <dt>**E \_ACCESSDENIED**</dt> </dl>         | 許可權錯誤，拒絕存取。<br/>                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**E \_OUTOFMEMORY**</dt> </dl>          | 系統資源限制，無法執行操作。<br/>                                                                                                                                                                                                                                                                 |
| <dl> <dt>**NAP \_ E \_ 不正確封 \_ 包**</dt> </dl>  | 如果傳回這個值，強制用戶端必須卸載封包（如果 NapAgent 傳回 NAP \_ 電子 \_ 不正確封包） \_ 。 在這種情況下，enforcer 必須假設正在交談的伺服器不是啟用 NAP 的，並且會從使用中的清單中移除連接 (也就是通知 NapAgent 線上狀態為 [關閉]) 。<br/> |
| <dl> <dt>**NAP \_ E 不符的 \_ \_ 識別碼**</dt> </dl>   | 如果傳回這個值，則表示 SoH-Response 封包中的相互關聯識別碼，與未處理的 SoH 回應不符。 在此情況下，enforcer 應該捨棄封包，並等候另一個較新的 SoH-Response 封包。<br/> 這可能是因回應較舊的要求訊息所造成。<br/>        |
| <dl> <dt>**NAP \_ E \_ 未 \_ 初始化**</dt> </dl> | Enforcer 先前尚未初始化。<br/>                                                                                                                                                                                                                                                                       |



 

## <a name="remarks"></a>備註

NapAgent 會從連線物件查詢 SoH-Response 資料 blob、處理它，然後設定產生的決策 (例如 連線物件上的完整/受限制存取/等) 。

強制用戶端必須先呼叫 [**INapEnforcementClientBinding：： Initialize**](inapenforcementclientbinding-initialize-method.md) 方法，才能呼叫這個或 [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) 介面的任何其他方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                      |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                                |
| 標頭<br/>                   | <dl> <dt>NapEnforcementClient。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapEnforcementClient .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>另請參閱

<dl> <dt>


</dt> <dt>

[**INapEnforcementClientBinding**](inapenforcementclientbinding.md)
</dt> <dt>

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> </dl>

 

 





