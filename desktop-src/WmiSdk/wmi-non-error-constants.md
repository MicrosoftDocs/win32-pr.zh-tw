---
description: 指出狀態且不表示錯誤的 WMI 傳回碼。
ms.assetid: 36faa3fb-9496-47ca-bdba-f8eb52a06ff7
ms.tgt_platform: multiple
title: WbemCli) 的 WMI 非錯誤常數 (
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0880c9fda00f03c1fa8b174242bfc84ed9d75ad8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192189"
---
# <a name="wmi-non-error-constants"></a>WMI 非錯誤常數

指出狀態且不表示錯誤的 WMI 傳回碼。

如果作業不會導致錯誤，WMI 會傳回下列其中一個程式碼做為 **HRESULT** ，指出作業的狀態。

> [!Note]  
> WMI 類別中的某些方法可以傳回系統和網路錯誤碼 (64，例如) 。 您可以在 [命令提示字元] 視窗中，使用 **net helpmsg** 命令檢查這些類型之錯誤碼的定義。 例如， **net helpmsg 64** 命令會傳回訊息：指定的網路名稱已無法再使用。

 

在 c + + 中，您可以呼叫 [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) 並指定 **C： \\ Windows \\ System32 \\ wbem \\wmiutils.dll** 作為訊息模組。

<dl> <dt>

<span id="WBEM_S_NO_ERROR"></span><span id="wbem_s_no_error"></span>**WBEM \_ S \_ 沒有 \_ 錯誤**
</dt> <dd> <dl> <dt>

0 (0x0) 
</dt> <dt>



作業成功。


</dt> </dl> </dd> <dt>

<span id="WBEM_S_FALSE"></span><span id="wbem_s_false"></span>**WBEM \_ S \_ FALSE**
</dt> <dd> <dl> <dt>

1 (0x1) 
</dt> <dt>



沒有其他可用的物件、傳回的物件數目小於要求的數目，或列舉的結尾。 當呼叫這個方法時，如果 *uCount* 參數的值為0，也會傳回此值。


</dt> </dl> </dd> <dt>

<span id="WBEM_S_ALREADY_EXISTS"></span><span id="wbem_s_already_exists"></span>**WBEM \_ S \_ 已經 \_ 存在**
</dt> <dd> <dl> <dt>

262145 (0x40001) 
</dt> <dt>



嘗試建立已存在的物件或類別。


</dt> </dl> </dd> <dt>

<span id="WBEM_S_RESET_TO_DEFAULT"></span><span id="wbem_s_reset_to_default"></span>**\_將 WBEM \_ 重設 \_ 為 \_ 預設值**
</dt> <dd> <dl> <dt>

262146 (0x40002) 
</dt> <dt>



所覆寫的屬性已刪除。 傳回這個值以表示原始的非覆寫值已還原為刪除的結果。


</dt> </dl> </dd> <dt>

<span id="WBEM_S_DIFFERENT"></span><span id="wbem_s_different"></span>**WBEM \_ S \_ 不同**
</dt> <dd> <dl> <dt>

262147 (0x40003) 
</dt> <dt>



要比較的物件、類別等專案 (物件、類別等) 不相同。


</dt> </dl> </dd> <dt>

<span id="WBEM_S_TIMEDOUT"></span><span id="wbem_s_timedout"></span>**WBEM \_ S \_ 逾時**
</dt> <dd> <dl> <dt>

262148 (0x40004) 
</dt> <dt>



呼叫超時。這不是錯誤狀況。 因此，可能也會傳回某些結果。


</dt> </dl> </dd> <dt>

<span id="WBEM_S_NO_MORE_DATA"></span><span id="wbem_s_no_more_data"></span>**WBEM \_ S \_ 沒有 \_ 其他 \_ 資料**
</dt> <dd> <dl> <dt>

262149 (0x40005) 
</dt> <dt>



列舉中沒有其他可用的資料，使用者必須終止列舉。


</dt> </dl> </dd> <dt>

<span id="WBEM_S_OPERATION_CANCELLED"></span><span id="wbem_s_operation_cancelled"></span>**WBEM \_ S 作業已 \_ \_ 取消**
</dt> <dd> <dl> <dt>

262150 (0x40006) 
</dt> <dt>



作業刻意或不慎取消。


</dt> </dl> </dd> <dt>

<span id="WBEM_S_PENDING"></span><span id="wbem_s_pending"></span>**WBEM \_ S \_ 擱置中**
</dt> <dd> <dl> <dt>

262151 (0x40007) 
</dt> <dt>



要求仍在進行中，但結果還無法使用。


</dt> </dl> </dd> <dt>

<span id="WBEM_S_DUPLICATE_OBJECTS"></span><span id="wbem_s_duplicate_objects"></span>**WBEM \_ S \_ 重複的 \_ 物件**
</dt> <dd> <dl> <dt>

262152 (0x40008) 
</dt> <dt>



在結果集 (Result Set) 中偵測出一個以上的相同物件。


</dt> </dl> </dd> <dt>

<span id="WBEM_S_ACCESS_DENIED"></span><span id="wbem_s_access_denied"></span>**WBEM \_ \_ 拒絕存取 \_**
</dt> <dd> <dl> <dt>

262153 (0x40009) 
</dt> <dt>



使用者被拒絕存取某些資源，但並非所有資源。


</dt> </dl> </dd> <dt>

<span id="WBEM_S_PARTIAL_RESULTS"></span><span id="wbem_s_partial_results"></span>**WBEM \_ S \_ 部分 \_ 結果**
</dt> <dd> <dl> <dt>

262160 (0x40010) 
</dt> <dt>



使用者未收到由於安全性違規) 以外的資源 (所要求的所有物件。


</dt> </dl> </dd> <dt>

<span id="WBEM_S_LIMITED_SERVICE"></span><span id="wbem_s_limited_service"></span>**WBEM \_ S \_ 受限 \_ 服務**
</dt> <dd> <dl> <dt>

274433 (0x43001) 
</dt> <dt>



提供者能夠提供有限的服務。


</dt> </dl> </dd> <dt>

<span id="WBEM_S_INDIRECTLY_UPDATED"></span><span id="wbem_s_indirectly_updated"></span>**\_ \_ \_ 已間接更新 WBEM**
</dt> <dd> <dl> <dt>

274434 (0x43002) 
</dt> <dt>



保留供未來使用。


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                               |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                         |
| 標頭<br/>                   | <dl> <dt>WbemCli。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WbemCli .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[WMI 傳回碼](wmi-return-codes.md)
</dt> </dl>

 

