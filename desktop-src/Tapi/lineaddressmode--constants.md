---
description: LINEADDRESSMODE \_ 位旗標常數描述線上路裝置上識別位址的各種方式。
ms.assetid: f0f132a0-2e8e-478f-909b-c100aa360daa
title: 'LINEADDRESSMODE_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e5e926772c82a36865c7f3b95c1ca1321db5682
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977532"
---
# <a name="lineaddressmode_-constants"></a>LINEADDRESSMODE \_ 常數

**LINEADDRESSMODE \_** 位旗標常數描述線上路裝置上識別位址的各種方式。

<dl> <dt>

<span id="LINEADDRESSMODE_ADDRESSID"></span><span id="lineaddressmode_addressid"></span>**LINEADDRESSMODE \_ ADDRESSID**
</dt> <dd> <dl> <dt>



使用範圍0至 *dwNumAddresses* 減去1的小整數來指定位址，其中 *dwNumAddresses* 是行裝置功能的值。


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSMODE_DIALABLEADDR"></span><span id="lineaddressmode_dialableaddr"></span>**LINEADDRESSMODE \_ DIALABLEADDR**
</dt> <dd> <dl> <dt>



位址是透過其電話號碼來指定。


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

您可以為裝置專屬的延伸模組指派高序位16位。 低序位16位是保留的。

這個常數用來選取要在其上產生呼叫的行位址。 一般模型會透過其位址識別碼來選取位址。 位址識別碼是用來在整個 TAPI 中識別位址的機制。 不過，在某些環境下進行呼叫時，使用電話號碼（而不是依位址識別碼）來識別來電的起始位址通常會更實用。 其中一個範例是透過一個具有許多位址的線路裝置，在交換器上將大量電臺 (協力廠商) 的可能模型化。 這一行代表所有工作站的集合，而且每個工作站都會對應到具有自己的主要電話號碼和位址識別碼的位址。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



 

 




