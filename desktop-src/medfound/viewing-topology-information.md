---
description: 查看拓撲資訊
ms.assetid: d687ecd3-9ad6-46d5-b927-d9b99af2002f
title: 查看拓撲資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bf29f28ac419da7df14d90efb50919634d7409b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468005"
---
# <a name="viewing-topology-information"></a>查看拓撲資訊

在 TopoEdit 中，每個拓撲專案（例如節點、節點輸入和節點輸出）都有一個相關聯的屬性存放區，可管理節點的行為。 若要查看屬性，請選取專案，[ **屬性] 窗格** 會顯示資訊。 針對從 XML 檔案載入的拓撲，某些節點可能不會顯示整個屬性存放區。 若要查看整個屬性存放區，請解決拓撲。 如需詳細資訊，請參閱 [使用 TopoEdit 解析拓撲](resolving-a-topology-with-topoedit.md)。

下表顯示拓撲專案和窗格所顯示的屬性。




| 拓撲專案 | 屬性 | 
|---------------|------------|
| 拓撲節點 | <ul><li>所有節點的<a href="topology-node-attributes.md">拓撲節點屬性</a>。<br /></li><li>僅適用于來源節點的<a href="presentation-descriptor-attributes.md">呈現描述項屬性</a>。<br /></li><li>轉換和輸出節點的輸入和輸出信任授權單位資訊。<br /></li></ul> | 
| 節點輸入 | <ul><li>所有節點的<a href="media-type-attributes.md">媒體類型屬性</a>。</li></ul> | 
| 節點輸出 | <ul><li>僅適用于來源節點的<a href="stream-descriptor-attributes.md">串流描述項屬性</a>。<br /></li><li>所有節點的<a href="media-type-attributes.md">媒體類型屬性</a>。<br /></li></ul> | 




 

除了指標參考和陣列值以外，屬性值可以變更。 若要變更屬性值，請輸入屬性旁的新值，然後按一下 [**屬性] 窗格** 上的 [**儲存**]。 新的值會在屬性存放區中更新，並只在解析之後套用至拓撲。

## <a name="to-add-a-new-attribute-for-a-node"></a>加入節點的新屬性

1.  按一下 [ **拓撲] 窗格** 上的節點，以選取該節點。

    節點上設定的屬性會顯示在 [ **屬性] 窗格** 中。

2.  在 [ **屬性] 窗格** 中，按一下 [ **新增**]。

    這會開啟 [ **加入屬性** ] 對話方塊。

3.  從第一個下拉式清單中，選擇 [屬性] 類別。

    這些分類相依于拓撲節點。 例如，針對來源節點，下拉式清單會顯示 **展示描述項屬性** 和 **節點屬性** 做為可用的類別。

4.  從第二個下拉式清單中，選擇您想要在節點上設定的屬性。

5.  在編輯方塊中，加入屬性的值。

6.  按一下 [ **新增** ] 以加入屬性並返回主視窗，或按一下 [ **取消** ] 取消作業。

7.  在 [ **拓撲** ] 功能表中，按一下 [ **解析拓撲** ]，將新屬性設定為拓撲。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 




