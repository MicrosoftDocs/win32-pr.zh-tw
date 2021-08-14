---
title: 卸載方法
description: 卸載方法
ms.assetid: 2ffaeea6-ff24-48b2-bc99-eba429434a30
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f74f274f758e34416cc73d82963fa21fbd93b14e7b6492c693f24b763081b49f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118474496"
---
# <a name="unload-method"></a>卸載方法

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

卸載指定字元的字元資料。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

*代理程式 ***。字元。卸載 "**_CharacterID_*_"_*

</dd> </dl>

## <a name="remarks"></a>備註

當您不再需要字元時，請使用這個方法來釋出用來儲存字元相關資訊的記憶體。 如果您再次存取此字元，請使用 [**Load**](load-method.md) 方法。

這個方法不會傳回 [**Request**](/windows/desktop/lwef/the-request-object) 物件。

 

 