---
title: HasOtherClients 屬性
description: HasOtherClients 屬性
ms.assetid: 5ecc6f42-786b-40a6-8800-9ad0d92edfb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf7bb91240ade815c00fb2e36adf1466dcb30ba4240be038342906be49e6ff2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118479003"
---
# <a name="hasotherclients-property"></a>HasOtherClients 屬性

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

傳回指定的字元是否正由其他應用程式使用中。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

*代理程式*。**( "**_CharacterID_*_" ) 的字元。HasOtherClients_*



| 值     | 描述                                |
|-----------|--------------------------------------------|
| **True**  | 字元有其他用戶端。           |
| **False** | 字元沒有其他用戶端。 |



 

</dd> </dl>

## <a name="remarks"></a>備註

當有多個應用程式正在共用 (載入) 相同的字元時，您可以使用這個屬性來判斷您的應用程式是否為唯一的字元或最後一個用戶端。

 

 




