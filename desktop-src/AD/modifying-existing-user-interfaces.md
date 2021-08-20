---
title: 修改現有的使用者介面
description: Active Directory 消費者和電腦 MMC 嵌入式管理單元的 [結果] 窗格會顯示容器內物件的幾個屬性資料行，例如 [名稱] 和 [描述] 屬性。
ms.assetid: 55f4ae82-c380-42a9-beba-047ffd0131eb
ms.tgt_platform: multiple
keywords:
- 修改現有的使用者介面 AD
- 使用者和電腦嵌入式管理單元 AD，修改顯示
- 使用者和電腦嵌入式管理單元 AD，新增資料行
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcf6ef4743009086ae19148c42a8addc5974e4ac833cdad8eee675fdce76a5f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025866"
---
# <a name="modifying-existing-user-interfaces"></a>修改現有的使用者介面

Active Directory 消費者和電腦 MMC 嵌入式管理單元的 [結果] 窗格會顯示容器內物件的幾個屬性資料行，例如 [ **名稱** ] 和 [ **描述** ] 屬性。 此嵌入式管理單元可讓使用者新增及移除嵌入式管理單元結果窗格中顯示的資料行。

若要變更顯示，使用者會使用 **View** 下拉式功能表，並選取 [ **新增/移除欄位**]。 在 [ **新增/移除資料行** ] 對話方塊中，有一份資料行清單可供使用者選擇，以顯示在 [結果] 窗格中。

隨附于 Windows Server 2003、Standard Edition、Windows server 2003、Enterprise Edition 和 Windows server 2003 Datacenter Edition 的 Active Directory 消費者和電腦 MMC 嵌入式管理單元，可讓您修改可在容器的嵌入式管理單元結果窗格中顯示的資料行清單。 如果嵌入式管理單元是以 Windows Server 2003 架構的樹系為目標，則這項功能才存在。

若要將資料行加入至清單，請在與屬性相關聯的物件類型中，將值加入至顯示規範的 **extraColumns** 屬性中。 **ExtraColumns** 屬性是多重值字串屬性，其中每個字串都採用下列格式。


```C++

<ldapdisplayname>,<column header>,<default visibility>,<width>,<unused>

```



下表列出這些值的內容。



| 值                        | 描述                                                                                                                         |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| " &lt; ldapdisplayname &gt; "    | 包含表示屬性之 **ldapDisplayName** 的字串。                                                         |
| " &lt; 資料行標題 &gt; "      | 包含字串，表示顯示在資料行標頭中的文字。                                                  |
| 「 &lt; 預設可見度 &gt; 」 | 如果預設為隱藏屬性，則包含數值 0; 如果預設為可見，則為1。               |
| 「 &lt; 寬度 &gt; 」              | 包含資料行的寬度（以圖元為單位）。 如果這個值是-1，則會將資料行的寬度設定為數據行標頭的寬度。 |
| 「 &lt; 未使用」 &gt;             | 未使用的。 必須為零。                                                                                                               |



 

例如，若要加入將在組織單位中顯示物件之正式名稱的資料行， **canonicalName** 屬性的值會加入至顯示規範容器中 **organizationalUnit-Display** 物件的 **extraColumns** 屬性。 加入至 **OrganizationalUnit 顯示** 物件之 **extraColumns** 屬性的字串看起來會像下面這樣。


```C++
canonicalName,Canonical Name,0,150,0
```



[**新增/移除資料行**] 對話方塊只會顯示所顯示之容器類型之 **DisplaySpecifier** 物件的 **extraColumns** 屬性所包含的資料行。 如果 [ **extraColumns** ] 屬性不包含任何值，[ **加入/移除資料行** ] 對話方塊會顯示一組固定的資料行。 一組固定的資料行複本包含在 **預設顯示** 物件的 **extraColumns** 屬性中。

若要將一或多個資料行加入特定物件的資料行清單中，您必須將所有的 **extraColumns** 值從 **預設的顯示** 物件複製到目標物件，然後加入自訂資料行。 如果您在指定類別上指定 **extraColumns** 屬性，則該類別會使用這些資料行，而且不會將它們與 **預設顯示** 類別中指定的資料行合併。 因此，對 **預設顯示** 類別的進一步變更將不會影響該物件。

若要針對未註冊任何自訂資料行的所有容器類型顯示自訂資料行，請將資料行的值加入 **預設顯示** 物件的 **extraColumns** 屬性中。

 

 




