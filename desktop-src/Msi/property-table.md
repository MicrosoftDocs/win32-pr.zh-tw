---
description: 屬性工作表包含安裝中所有已定義屬性的屬性名稱和值。 具有 Null 值的屬性不會出現在資料表中。
ms.assetid: 1f4215b2-dc71-4e6e-bc2e-3b43316806b9
title: 屬性工作表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 612ab63aa36de6cf91ec8176eefec84cef591c55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692963"
---
# <a name="property-table"></a>屬性工作表

屬性工作表包含安裝中所有已定義屬性的屬性名稱和值。 具有 Null 值的屬性不會出現在資料表中。

屬性資料表具有下列資料行。



| Column   | 類型                         | 答案 | Nullable |
|----------|------------------------------|-----|----------|
| 屬性 | [識別碼](identifier.md) | Y   | N        |
| 值    | [Text](text.md)             | N   | N        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>財產
</dt> <dd>

屬性的名稱。 請參閱 [屬性](properties.md)。

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>價值
</dt> <dd>

屬性的可當地語系化字串值。 這可能永遠不會是 Null 或空字串。

</dd> </dl>

## <a name="remarks"></a>備註

請注意，您不能使用屬性工作表將屬性設為另一個屬性的值。 安裝程式在屬性資料行中設定屬性之前，不會對 [值] 資料行中輸入的文字字串執行任何動作。 如果在屬性資料行中輸入 FirstProperty \[ ，並 \] 在 [值] 資料行中 SecondProperty，則 FirstProperty 的值會設定為文字字串 " \[ SecondProperty \] "，而非 SecondProperty 屬性的值。 這是防止在屬性工作表中建立迴圈參考的必要動作。 相反地，您可以使用 [自訂動作類型 51](custom-action-type-51.md)，將一個屬性設定為另一個。

請注意， [**AdminProperties**](adminproperties.md) 屬性可以用來覆寫 [系統管理安裝](administrative-installation.md)期間屬性工作表中的值。

請勿將屬性用於密碼或其他必須保持安全的資訊。 安裝程式可以將撰寫的屬性值寫入至記錄檔或系統登錄中，或在執行時間建立的屬性值。

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE05](ice05.md)  
[ICE06](ice06.md)  
[ICE16](ice16.md)  
[ICE24](ice24.md)  
[ICE31](ice31.md)  
[ICE34](ice34.md)  
[ICE36](ice36.md)  
[ICE40](ice40.md)  
[ICE46](ice46.md)  
[ICE48](ice48.md)  
[ICE52](ice52.md)  
[ICE61](ice61.md)  
[ICE73](ice73.md)  
[ICE74](ice74.md)  
[ICE80](ice80.md)  
[ICE87](ice87.md)  
[ICE88](ice88.md)  
[ICE91](ice91.md)  
[ICE99](ice99.md)  
</dl>

 

 



