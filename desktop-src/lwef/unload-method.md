---
title: 卸載方法
description: 卸載方法
ms.assetid: 2ffaeea6-ff24-48b2-bc99-eba429434a30
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41d19f5f29647ff01b5a52bd8978694aaef1c43a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103682011"
---
# <a name="unload-method"></a>卸載方法

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

卸載指定字元的字元資料。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

*代理程式 ***。字元。 Unload "*** CharacterID * * *"**

</dd> </dl>

## <a name="remarks"></a>備註

當您不再需要字元時，請使用這個方法來釋出用來儲存字元相關資訊的記憶體。 如果您再次存取此字元，請使用 [**Load**](load-method.md) 方法。

這個方法不會傳回 [**Request**](/windows/desktop/lwef/the-request-object) 物件。

 

 