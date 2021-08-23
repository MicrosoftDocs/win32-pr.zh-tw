---
title: IdleStart 事件
description: IdleStart 事件
ms.assetid: 3d97c26b-b88a-42e3-9072-0bc65510efc2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81458d4c88bc5db4ae4231ecb4ca47f456700917f42d6ccdfe5a6013bc288849
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119716048"
---
# <a name="idlestart-event"></a>IdleStart 事件

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

當伺服器將字元設定為 **閒置** 狀態時發生。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

**子***代理程式 * * * \_ IdleStart* *  **(ByVal** *CharacterID * * * )**



| 部分          | 描述                                         |
|---------------|-----------------------------------------------------|
| *CharacterID* | 以字串形式傳回閒置字元的識別碼。 |



 

</dd> </dl>

### <a name="remarks"></a>備註

伺服器會將此事件傳送給該字元的所有用戶端。

### <a name="see-also"></a>另請參閱

[**IdleComplete 事件**](idlecomplete-event.md)


 

 




