---
description: LINEADDRFEATURE \_ 常數會列出可在位址上叫用的作業。
ms.assetid: dedeee7b-578b-4b19-8b99-5cd23779d661
title: 'LINEADDRFEATURE_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 825902c2943806d1d495e14a0f0a5042f2949796
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982616"
---
# <a name="lineaddrfeature_-constants"></a>LINEADDRFEATURE \_ 常數

**LINEADDRFEATURE \_** 常數會列出可在位址上叫用的作業。

<dl> <dt>

<span id="LINEADDRFEATURE_FORWARD"></span><span id="lineaddrfeature_forward"></span>**\_向前 LINEADDRFEATURE**
</dt> <dd> <dl> <dt>



可以轉送位址。


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_MAKECALL"></span><span id="lineaddrfeature_makecall"></span>**LINEADDRFEATURE \_ MAKECALL**
</dt> <dd> <dl> <dt>



撥出電話可以放在位址上。


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_PICKUP"></span><span id="lineaddrfeature_pickup"></span>**LINEADDRFEATURE \_ 取貨**
</dt> <dd> <dl> <dt>



您可以在位址上挑選通話。


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_PICKUPDIRECT"></span><span id="lineaddrfeature_pickupdirect"></span>**LINEADDRFEATURE \_ PICKUPDIRECT**
</dt> <dd> <dl> <dt>



[**LinePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup)函式可用來收取特定位址的呼叫。


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_PICKUPGROUP"></span><span id="lineaddrfeature_pickupgroup"></span>**LINEADDRFEATURE \_ PICKUPGROUP**
</dt> <dd> <dl> <dt>



您可以使用 [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) 函式來挑選群組中的呼叫。


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_PICKUPHELD"></span><span id="lineaddrfeature_pickupheld"></span>**LINEADDRFEATURE \_ PICKUPHELD**
</dt> <dd> <dl> <dt>



具有 **null** 目的地位址的 [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup)函式 () 可用來收取位址上保留的呼叫。 這通常只會用於橋接專屬的相片順序。


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_PICKUPWAITING"></span><span id="lineaddrfeature_pickupwaiting"></span>**LINEADDRFEATURE \_ PICKUPWAITING**
</dt> <dd> <dl> <dt>



具有 **null** 目的地位址的 [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup)函式 () 可用來收取通話等候呼叫。 請注意，這不一定表示等候中的呼叫真的存在，因為電話語音裝置通常無法自動偵測這類呼叫;但是，它會指出將會叫用攔截-flash 函式，以嘗試切換到這類呼叫。


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_SETMEDIACONTROL"></span><span id="lineaddrfeature_setmediacontrol"></span>**LINEADDRFEATURE \_ SETMEDIACONTROL**
</dt> <dd> <dl> <dt>



您可以在此位址上設定媒體控制項。


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_SETTERMINAL"></span><span id="lineaddrfeature_setterminal"></span>**LINEADDRFEATURE \_ SETTERMINAL**
</dt> <dd> <dl> <dt>



您可以設定此位址的終端模式。


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_SETUPCONF"></span><span id="lineaddrfeature_setupconf"></span>**LINEADDRFEATURE \_ SETUPCONF**
</dt> <dd> <dl> <dt>



具有 **Null** 初始呼叫的電話會議可以在這個位址設定。


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_UNCOMPLETECALL"></span><span id="lineaddrfeature_uncompletecall"></span>**LINEADDRFEATURE \_ UNCOMPLETECALL**
</dt> <dd> <dl> <dt>



呼叫完成要求可以在此位址取消。


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_UNPARK"></span><span id="lineaddrfeature_unpark"></span>**LINEADDRFEATURE \_ UNPARK**
</dt> <dd> <dl> <dt>



您可以使用此位址來離開呼叫。

> [!Note]  
> 如果未在 [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus)的 **dwAddressFeatures** 成員中設定新修改過的「取貨」位 \_ ，但已設定 LINEADDRFEATURE 取貨位，則任何收取模式都可以運作; 服務提供者只是未指定哪一個。

 


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_FORWARDDND"></span><span id="lineaddrfeature_forwarddnd"></span>**LINEADDRFEATURE \_ FORWARDDND**
</dt> <dd> <dl> <dt>



[**LineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward)函式 (有空白的目的地位址) 可用來開啟位址上的「請勿打擾」功能。 \_也會設定 LINEADDRFEATURE 轉寄。


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_FORWARDFWD"></span><span id="lineaddrfeature_forwardfwd"></span>**LINEADDRFEATURE \_ FORWARDFWD**
</dt> <dd> <dl> <dt>



[**LineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward)函式可以用來將位址上的呼叫轉送到其他數位。 \_也會設定 LINEADDRFEATURE 轉寄。

> [!Note]  
> 如果在 [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus)的 **dwAddressFeatures** 成員中未設定新的已修改 "FORWARD" 位 \_ ，但已設定 LINEADDRFEATURE 轉寄位，則任何轉寄模式都可以運作，而服務提供者只會指定哪一個。

 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

無延伸。 所有32位都是保留的。

這個常數會在 [**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)) 和 [**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus)) 所傳回的 [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) (所傳回的 [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) (中使用。 **LINEADDRESSCAPS** 會報告服務提供者的位址功能可用性， (主要是指定位址的交換器) 。 應用程式會在初始化時進行這項判斷。 [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus)結構會報告指定的位址，當地址處於目前狀態時，可以實際叫用的位址功能。 在位址狀態變更之後，應用程式會以動態方式進行判斷，通常是由位址上的呼叫相關活動所造成。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus)
</dt> <dt>

[**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward)
</dt> <dt>

[**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)
</dt> <dt>

[**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus)
</dt> <dt>

[**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup)
</dt> </dl>

 

 




