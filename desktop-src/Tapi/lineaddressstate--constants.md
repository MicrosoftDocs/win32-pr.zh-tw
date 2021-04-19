---
description: LINEADDRESSSTATE \_ 位旗標常數描述各種位址狀態專案。
ms.assetid: f06140d0-f41a-4228-93c5-21d609af5473
title: 'LINEADDRESSSTATE_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 483ac665c41989c65b43419442601dfb70667dc2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000984"
---
# <a name="lineaddressstate_-constants"></a>LINEADDRESSSTATE \_ 常數

**LINEADDRESSSTATE \_** 位旗標常數描述各種位址狀態專案。

<dl> <dt>

<span id="LINEADDRESSSTATE_CAPSCHANGE"></span><span id="lineaddressstate_capschange"></span>**LINEADDRESSSTATE \_ CAPSCHANGE**
</dt> <dd> <dl> <dt>



指出，由於使用者或其他情況所做的設定變更，位址的 [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) 結構中有一或多個成員已變更。 應用程式應該使用 [**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps) 來讀取更新的結構。 如果服務提供者將包含此值的 [**行 \_ ADDRESSSTATE**](line-addressstate.md) 訊息傳送至 tapi，tapi 會將它傳遞至已協商 tapi 1.4 版或更新版本的應用程式; 協調先前 API 版本的應用程式將會收到指定 LINEDEVSTATE 重新初始化的 [**行 \_ LINEDEVSTATE**](line-linedevstate.md) 訊息 \_ ，要求使用者將其關機並重新初始化，以取得更新的資訊。


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_DEVSPECIFIC"></span><span id="lineaddressstate_devspecific"></span>**LINEADDRESSSTATE \_ DEVSPECIFIC**
</dt> <dd> <dl> <dt>



位址狀態的裝置特定專案已變更。


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_FORWARD"></span><span id="lineaddressstate_forward"></span>**\_向前 LINEADDRESSSTATE**
</dt> <dd> <dl> <dt>



位址的轉送狀態已變更，包括判斷無回應條件的環形數。 應用程式應該檢查位址狀態，以判斷位址目前轉送狀態的詳細資料。


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_INUSEMANY"></span><span id="lineaddressstate_inusemany"></span>**LINEADDRESSSTATE \_ INUSEMANY**
</dt> <dd> <dl> <dt>



受監視或橋接的位址已變更，而不是由一個工作站使用於一個以上的工作站。


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_INUSEONE"></span><span id="lineaddressstate_inuseone"></span>**LINEADDRESSSTATE \_ INUSEONE**
</dt> <dd> <dl> <dt>



位址已從閒置狀態變更，或由許多橋接的電臺使用，只供一個站使用。


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_INUSEZERO"></span><span id="lineaddressstate_inusezero"></span>**LINEADDRESSSTATE \_ INUSEZERO**
</dt> <dd> <dl> <dt>



位址已變更為閒置 (它未由任何工作站) 使用中。


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_NUMCALLS"></span><span id="lineaddressstate_numcalls"></span>**LINEADDRESSSTATE \_ NUMCALLS**
</dt> <dd> <dl> <dt>



位址上的呼叫數目已變更。 這是事件的結果，例如新的來電、位址上的外寄呼叫，或變更其保存狀態的呼叫。 此旗標涵蓋 [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus)結構中任何成員 **dwNumActiveCalls**、 **dwNumOnHoldCalls** 和 **dwNumOnHoldPendingCalls** 的變更。 當應用程式收到 [**一行 \_ ADDRESSSTATE**](line-addressstate.md) (numCalls) 訊息時，應用程式應該會檢查這三個成員。


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_OTHER"></span><span id="lineaddressstate_other"></span>**LINEADDRESSSTATE \_ 其他**
</dt> <dd> <dl> <dt>



位址-下列以外的狀態專案已變更。 應用程式應該檢查目前的位址狀態，以判斷哪些專案已經變更。


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSTATE_TERMINALS"></span><span id="lineaddressstate_terminals"></span>**LINEADDRESSSTATE \_ 終端機**
</dt> <dd> <dl> <dt>



位址的終端機設定已變更。


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

無延伸。 所有32位都是保留的。

在 [**\_ ADDRESSSTATE**](line-addressstate.md) 訊息中，會通知應用程式這些狀態專案的變更。 位址的裝置功能指出可能為此位址報告的位址狀態變更。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**行 \_ ADDRESSSTATE**](line-addressstate.md)
</dt> <dt>

[**行 \_ LINEDEVSTATE**](line-linedevstate.md)
</dt> <dt>

[**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus)
</dt> <dt>

[**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)
</dt> </dl>

 

 




