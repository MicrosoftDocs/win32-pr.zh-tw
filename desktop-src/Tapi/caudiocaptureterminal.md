---
description: CAudioCaptureTerminal 終端機衍生自 CSingleFilterTerminal，並使用 DirectShow wavein 篩選器來為 wave 裝置實行靜態音訊捕獲終端機。 大部分的 Msp 都不需要覆寫此終端機的執行。
ms.assetid: 2860bf22-46ae-484a-a47b-0d7057b900a1
title: CAudioCaptureTerminal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 308af17ce7a7cb4d2d4cadebb43b06437ec14abc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990329"
---
# <a name="caudiocaptureterminal"></a>CAudioCaptureTerminal

**CAudioCaptureTerminal** 終端機衍生自 [CSingleFilterTerminal](csinglefilterterminal.md) ，並使用 DirectShow wavein 篩選器來為 wave 裝置實行靜態音訊捕獲終端機。 大部分的 Msp 都不需要覆寫此終端機的執行。

定義于 MSPtmac 中。

## <a name="remarks"></a>備註

**CAudioCaptureTerminal** 的 [**put \_ 餘額**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-put_balance)和 [**取得 \_ 餘額**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-get_balance)方法不會實作為，並會傳回電子 \_ >notimpl。

 

 



