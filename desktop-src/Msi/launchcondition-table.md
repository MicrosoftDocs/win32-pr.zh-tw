---
description: LaunchConditions 動作會使用 LaunchCondition 資料表。 它包含一份條件清單，必須滿足這些條件才能開始安裝。
ms.assetid: 6e550cc7-c479-417e-ab89-882d8fece4e1
title: LaunchCondition 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d67834f058575dde297454480040028ef9c5732
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991824"
---
# <a name="launchcondition-table"></a>LaunchCondition 資料表

[LaunchConditions 動作](launchconditions-action.md)會使用 LaunchCondition 資料表。 它包含一份條件清單，必須滿足這些條件才能開始安裝。

LaunchCondition 資料表具有下列資料行。



| Column      | 類型                       | 答案 | Nullable |
|-------------|----------------------------|-----|----------|
| 條件   | [Condition](condition.md) | Y   | N        |
| Description | [格式 化](formatted.md) | N   | N        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>條件
</dt> <dd>

必須評估為 True 的運算式，才能開始安裝。

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>描述
</dt> <dd>

當條件失敗且必須終止安裝時，可顯示的可當地語系化文字。

</dd> </dl>

## <a name="remarks"></a>備註

您無法保證藉由撰寫此資料表來評估啟動條件的順序。 如果需要控制評估條件的順序，您應該在安裝中使用自訂動作類型19自訂動作來執行此動作。

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE46](ice46.md)  
[ICE79](ice79.md)  
[ICE86](ice86.md)  
</dl>

 

 



