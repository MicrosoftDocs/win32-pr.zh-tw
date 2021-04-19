---
description: CAudioRenderTerminal 終端機衍生自 CSingleFilterTerminal，並使用 DirectShow waveout 篩選器來為 wave 裝置實行靜態音訊轉譯終端機。 大部分的 Msp 都不需要覆寫此終端機的執行。
ms.assetid: 58cd0765-9430-4333-ae96-4d8ca73727b5
title: CAudioRenderTerminal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad9915ef03a210f4ca440cb7a7b66448228b41df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984595"
---
# <a name="caudiorenderterminal"></a>CAudioRenderTerminal

**CAudioRenderTerminal** 終端機衍生自 [CSingleFilterTerminal](csinglefilterterminal.md) ，並使用 DirectShow waveout 篩選器來為 wave 裝置實行靜態音訊轉譯終端機。 大部分的 Msp 都不需要覆寫此終端機的執行。

定義于 MSPtrmar 中。

## <a name="remarks"></a>備註

**CAudioRenderTerminal** 的 [**put \_ 餘額**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-put_balance)和 [**取得 \_ 餘額**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-get_balance)方法不會實作為，並會傳回電子 \_ >notimpl。

 

 



