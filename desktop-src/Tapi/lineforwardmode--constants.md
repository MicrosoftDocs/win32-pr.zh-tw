---
description: LINEFORWARDMODE \_ 位旗標常數描述可轉送位址之呼叫的條件。
ms.assetid: 8cc053bd-1056-42be-b48a-d2312c456893
title: 'LINEFORWARDMODE_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33702be12afaef5d1194ca5c0d288bd967a93e2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984760"
---
# <a name="lineforwardmode_-constants"></a>LINEFORWARDMODE \_ 常數

**LINEFORWARDMODE \_** 位旗標常數描述可轉送位址之呼叫的條件。

<dl> <dt>

<span id="LINEFORWARDMODE_BUSY"></span><span id="lineforwardmode_busy"></span>**LINEFORWARDMODE \_ 忙碌**
</dt> <dd> <dl> <dt>



將所有呼叫轉寄于忙碌狀態，而不考慮其來源。 當對忙碌中的內部和外部呼叫進行轉送，而且無法另外控制時，請使用此值。


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_BUSYEXTERNAL"></span><span id="lineforwardmode_busyexternal"></span>**LINEFORWARDMODE \_ BUSYEXTERNAL**
</dt> <dd> <dl> <dt>



將所有外部呼叫轉寄于忙碌中。 當對忙碌中的內部和外部呼叫進行轉送，而且沒有任何答案可以個別控制時，請使用此值。


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_BUSYINTERNAL"></span><span id="lineforwardmode_busyinternal"></span>**LINEFORWARDMODE \_ BUSYINTERNAL**
</dt> <dd> <dl> <dt>



將所有內部呼叫轉寄于忙碌中。 當對忙碌中的內部和外部呼叫進行轉送，而且沒有任何答案可以個別控制時，請使用此值。


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_BUSYNA"></span><span id="lineforwardmode_busyna"></span>**LINEFORWARDMODE \_ BUSYNA**
</dt> <dd> <dl> <dt>



將所有呼叫轉寄于忙碌/沒有回應，而不論其來源。 當對忙碌中的內部和外部呼叫進行轉送，而且無法另外控制時，請使用此值。


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_BUSYNAEXTERNAL"></span><span id="lineforwardmode_busynaexternal"></span>**LINEFORWARDMODE \_ BUSYNAEXTERNAL**
</dt> <dd> <dl> <dt>



將所有外部呼叫轉寄于忙碌/沒有回應。 當待命上的呼叫轉送，而且無法針對內部呼叫分開控制時，請使用此值。


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_BUSYNAINTERNAL"></span><span id="lineforwardmode_busynainternal"></span>**LINEFORWARDMODE \_ BUSYNAINTERNAL**
</dt> <dd> <dl> <dt>



將所有內部呼叫轉寄于忙碌/沒有回應。 當待命上的呼叫轉送，而且無法針對內部呼叫分開控制時，請使用此值。


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_BUSYNASPECIFIC"></span><span id="lineforwardmode_busynaspecific"></span>**LINEFORWARDMODE \_ BUSYNASPECIFIC**
</dt> <dd> <dl> <dt>



在忙碌/沒有回應的情況中，會在指定的位址 (選擇性呼叫轉送) 發出的所有呼叫。


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_BUSYSPECIFIC"></span><span id="lineforwardmode_busyspecific"></span>**LINEFORWARDMODE \_ BUSYSPECIFIC**
</dt> <dd> <dl> <dt>



將源自指定位址的所有呼叫轉寄 (選擇性呼叫轉送) 。


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_NOANSW"></span><span id="lineforwardmode_noansw"></span>**LINEFORWARDMODE \_ NOANSW**
</dt> <dd> <dl> <dt>



將所有呼叫轉寄于沒有答案的位置，而不管其來源。 當內部和外部呼叫的呼叫轉送無法分開控制時，請使用此值。


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_NOANSWEXTERNAL"></span><span id="lineforwardmode_noanswexternal"></span>**LINEFORWARDMODE \_ NOANSWEXTERNAL**
</dt> <dd> <dl> <dt>



將所有外部呼叫轉寄于無回應。 當無法接聽內部和外部呼叫的時，請使用此值來分開控制。


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_NOANSWINTERNAL"></span><span id="lineforwardmode_noanswinternal"></span>**LINEFORWARDMODE \_ NOANSWINTERNAL**
</dt> <dd> <dl> <dt>



轉寄所有內部呼叫，而不接聽。 當無法接聽內部和外部呼叫的時，請使用此值來分開控制。


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_NOANSWSPECIFIC"></span><span id="lineforwardmode_noanswspecific"></span>**LINEFORWARDMODE \_ NOANSWSPECIFIC**
</dt> <dd> <dl> <dt>



將發出于指定位址的所有呼叫轉寄 (選擇性呼叫轉送) 。


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_UNAVAIL"></span><span id="lineforwardmode_unavail"></span>**LINEFORWARDMODE \_ UNAVAIL**
</dt> <dd> <dl> <dt>



呼叫會轉送，但在發生轉送的情況下，並不知道將會發生轉送，而且服務提供者永遠不知道。  (TAPI 1.4 版和更新版本) 


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_UNCOND"></span><span id="lineforwardmode_uncond"></span>**LINEFORWARDMODE \_ UNCOND**
</dt> <dd> <dl> <dt>



無條件轉寄所有呼叫，而不考慮其來源。 當內部和外部呼叫的無條件轉送無法分開控制時，請使用此值。 無條件轉送會覆寫在忙碌及/或沒有回應狀況時的轉送。


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_UNCONDEXTERNAL"></span><span id="lineforwardmode_uncondexternal"></span>**LINEFORWARDMODE \_ UNCONDEXTERNAL**
</dt> <dd> <dl> <dt>



無條件轉寄所有外部呼叫。 當內部和外部呼叫的無條件轉送可以個別控制時，請使用此值。


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_UNCONDINTERNAL"></span><span id="lineforwardmode_uncondinternal"></span>**LINEFORWARDMODE \_ UNCONDINTERNAL**
</dt> <dd> <dl> <dt>



無條件轉送所有內部呼叫。 當內部和外部呼叫的無條件轉送可以個別控制時，請使用此值。


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_UNCONDSPECIFIC"></span><span id="lineforwardmode_uncondspecific"></span>**LINEFORWARDMODE \_ UNCONDSPECIFIC**
</dt> <dd> <dl> <dt>



將源自指定位址的所有呼叫無條件轉寄 (選擇性呼叫轉送) 。


</dt> </dl> </dd> <dt>

<span id="LINEFORWARDMODE_UNKNOWN"></span><span id="lineforwardmode_unknown"></span>**LINEFORWARDMODE \_ 不明**
</dt> <dd> <dl> <dt>



呼叫會轉送，但目前不知道轉送發生的條件。 未來可能會有已知的狀況。  (TAPI 1.4 版和更新版本) 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

無延伸。 所有32位都是保留的。

LINEFORWARDMODE 所定義的位旗標 \_ 不是直角。 無條件轉送會忽略任何特定的狀況，例如忙碌或沒有回應。 如果無條件轉寄沒有作用，則在忙碌和沒有回應的情況下進行轉送，可以個別或個別控制。 如果個別控制，則 \_ 可以另外使用 LINEFORWARDMODE 忙碌和 LINEFORWARDMODE \_ NOANSW 旗標。 如果未另外控制，則必須使用旗標 LINEFORWARDMODE \_ BUSYNA。 同樣地，如果內部和外部呼叫的轉送可以個別控制，則 \_ 可以個別使用 LINEFORWARDMODE internal 和 LINEFORWARDMODE \_ 外部旗標，否則會使用組合。

位址功能指出指派給一行的每個位址都有哪些轉送模式可用。 應用程式可以使用 [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) 在交換器設定轉送條件。

為了回溯相容性，服務提供者必須負責檢查該行上的已協商 API 版本，如果協商的版本不支援，則不會使用這些 LINEFORWARDMODE \_ 值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



 

 




