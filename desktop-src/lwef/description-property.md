---
title: 'Description 屬性 (舊版 Windows 環境功能) '
description: Description 屬性
ms.assetid: 81ac4bc7-ef0c-4e7c-b57e-acc4ad315515
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da7ff293af98303fa0dab97aca76ed169123ea229c1fc70c156ef2c099472157
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118751990"
---
# <a name="description-property-legacy-windows-environment-features"></a>Description 屬性 (舊版 Windows 環境功能) 

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

傳回或設定字串，這個字串會指定指定字元的描述。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

*代理程式*。**( "**_CharacterID_*_" ) 的字元。描述_* \[  =  *字串*\]



| 部分     | 描述                                                                                    |
|----------|------------------------------------------------------------------------------------------------|
| *string* | 字串值，對應到目前語言設定)  (字元的描述。 |



 

</dd> </dl>

## <a name="remarks"></a>備註

字元的 **描述** 可能取決於字元的 **LanguageID** 設定。 一種語言的字元名稱可能不同，或使用不同于另一個語言的字元。 使用 Microsoft Agent 字元編輯器來編譯字元時，會定義特定語言的字元預設 **描述** 。

> [!Note]  
> [ **描述** ] 屬性設定為選擇性，而且可能不會提供給所有字元。

 

 

 




