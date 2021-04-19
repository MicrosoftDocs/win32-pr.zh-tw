---
description: LINETRANSLATEOPTION \_ 位旗標常數描述位址轉譯使用的選項。
ms.assetid: 3f5e9952-945e-42b8-8536-b52a0c833282
title: 'LINETRANSLATEOPTION_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac1e103f2a93d30be5260b27c7bf5c0e97f3ce7a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000790"
---
# <a name="linetranslateoption_-constants"></a>LINETRANSLATEOPTION \_ 常數

**LINETRANSLATEOPTION \_** 位旗標常數描述位址轉譯使用的選項。

<dl> <dt>

<span id="LINETRANSLATEOPTION_CANCELCALLWAITING"></span><span id="linetranslateoption_cancelcallwaiting"></span>**LINETRANSLATEOPTION \_ CANCELCALLWAITING**
</dt> <dd> <dl> <dt>



如果為位置定義了取消呼叫等候字串，則設定此位將會導致該字串插入可撥出的字串開頭。 這通常是由資料數據機和傳真應用程式所使用，以防止呼叫等候嗶聲的電話中斷。 如果沒有為位置定義取消呼叫等候字串，這個位就不會有任何影響。 請注意，使用此位的應用程式也會 \_ 在 [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams)結構的 **dwCallParamFlags** 成員中，透過 *lpCallParams* 參數 [**來設定**](/windows/desktop/api/Tapi/nf-tapi-linemakecall)LINECALLPARAMFLAGS 安全位，如此一來，如果線路裝置使用可撥數位以外的機制來隱藏呼叫中斷，則會叫用該機制。


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATEOPTION_CARDOVERRIDE"></span><span id="linetranslateoption_cardoverride"></span>**LINETRANSLATEOPTION \_ CARDOVERRIDE**
</dt> <dd> <dl> <dt>



預設的電話卡會以指定的電話卡覆寫。


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATEOPTION_FORCELD"></span><span id="linetranslateoption_forceld"></span>**LINETRANSLATEOPTION \_ FORCELD**
</dt> <dd> <dl> <dt>



此選項會強制將位址 () 轉譯為長距離。


</dt> </dl> </dd> <dt>

<span id="LINETRANSLATEOPTION_FORCELOCAL"></span><span id="linetranslateoption_forcelocal"></span>**LINETRANSLATEOPTION \_ FORCELOCAL**
</dt> <dd> <dl> <dt>



此選項會強制將 (位址) 的數目轉譯為本機。


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

無延伸。 所有32位都是保留的。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams)
</dt> <dt>

[**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[**LINETRANSLATEOUTPUT**](/windows/desktop/api/Tapi/ns-tapi-linetranslateoutput)
</dt> </dl>

 

 




