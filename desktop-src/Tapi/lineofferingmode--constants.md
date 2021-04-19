---
description: LINEOFFERINGMODE \_ 位旗標常數 (TAPI 1.4 版和更新版本，) 描述供應專案呼叫的不同 substates。
ms.assetid: a6c6d30f-fdc4-4ba5-b1a2-3c709445aedc
title: 'LINEOFFERINGMODE_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b9e04720b4ea79f5b169e4a279a3af2e0cdda39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996231"
---
# <a name="lineofferingmode_-constants"></a>LINEOFFERINGMODE \_ 常數

**LINEOFFERINGMODE \_** 位旗標常數 (TAPI 1.4 版和更新版本，) 描述供應專案呼叫的不同 substates。 在提供撥號狀態 trdansitions 之後，您可以使用模式作為應用程式的撥號狀態，而在 [**\_ CALLSTATE**](line-callstate.md) 訊息中指出呼叫是在 LINECALLSTATE 供應專案中 \_ 。 當呼叫位於與其他工作站 (橋接) 的共用位址時，就會使用這些值 (查看 [**LINEADDRESSSHARING \_ 常數**](lineaddresssharing--constants.md)) ，主要是電子關鍵系統。

<dl> <dt>

<span id="LINEOFFERINGMODE_ACTIVE"></span><span id="lineofferingmode_active"></span>**LINEOFFERINGMODE \_ 使用中**
</dt> <dd> <dl> <dt>



表示在目前工作站上發出的呼叫 (會伴隨 LINEDEVSTATE \_ 響鈴訊息) ，而且如果有任何應用程式設定為自動回答，則可以這樣做。 如果撥號狀態模式為零，則應用程式應該假設該值為使用中 (這會是非橋接位址) 上的情況。  (TAPI 1.4 版和更新版本) 


</dt> </dl> </dd> <dt>

<span id="LINEOFFERINGMODE_INACTIVE"></span><span id="lineofferingmode_inactive"></span>**LINEOFFERINGMODE \_ 非使用中**
</dt> <dd> <dl> <dt>



指出會在多個工作站上提供呼叫，但目前的工作站不會發出警示 (例如，它可能是供應專案狀態為「諮詢」的一站，例如閃爍的燈) ;工作站上設定自動接聽的軟體應最好不要接聽電話，因為這應該是主要 (警示) 站的特權用，但 [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer) 可能用來連接電話。  (TAPI 1.4 版和更新版本) 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

不可延伸。 所有32位都是保留的。

為了回溯相容性，服務提供者必須負責檢查該行上的已協商 API 版本，如果已協商的版本不支援，則不會使用這些 LINEOFFERINGMODE \_ 值。 未 cognizant LINEOFFERINGMODE 的應用程式 \_ 很有可能會假設 LINECALLSTATE 供應專案中的呼叫位於 \_ LINEOFFERINGMODE \_ ACTIVE 中。

\_ \_ 當呼叫位於與其他工作站共用 (橋接的位址時，會使用 LINEOFFERINGMODE ACTIVE 和 LINEOFFERINGMODE 非使用中的值; 請參閱[LINEADDRESSSHARING \_ 常數](lineaddresssharing--constants.md)) ，主要是電子金鑰系統。 如果供應專案通話狀態模式為「作用中」，這表示呼叫會在目前的工作站上發出警示 (將會伴隨 LINEDEVSTATE \_ 響鈴訊息) ，而且如果有任何應用程式設定為自動回答，則可以這樣做。 如果通話狀態模式為「非使用中」，則會在一個以上的工作站上提供呼叫，但目前的工作站不會發出警示 (例如，它可能是供應專案狀態為「諮詢」的通知站，例如閃爍燈的) ;工作站上設定自動接聽的軟體應最好不要接聽電話，因為這應該是主要 (警示) 站上的特權用，但 [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer) 可以用來連線通話。 如果撥號狀態模式為零，則應用程式應該假設該值為使用中 (這會是非橋接位址) 上的情況。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



 

 




