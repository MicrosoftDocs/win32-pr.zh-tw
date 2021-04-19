---
description: 您可以從兩個不同的觀點參考叢集：在檔案和磁片區中。
ms.assetid: 8e999524-4fe9-49b0-8b59-081fa7a42c72
title: 叢集和延伸區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e6b379e0dbc4f70ccf001f0be0517e25c0c99a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106974475"
---
# <a name="clusters-and-extents"></a>叢集和延伸區

您可以從兩個不同的觀點參考叢集：在檔案和磁片區中。 檔案中的任何叢集都有 *虛擬叢集編號* (的 VCN) ，也就是從檔案開頭起算的相對位移。 例如，搜尋至叢集大小的兩倍，然後再讀取，將會傳回從第三個 VCN 開始的資料。 *邏輯叢集編號* (LCN) 描述叢集與磁片區中某個任意點的位移。 LCNs 只能視為序數或相對的數位。 邏輯群集不保證會對應到實體硬碟的磁區。

*範圍* 是連續叢集的執行。 例如，假設包含30個叢集的檔案記錄在兩個範圍內。 第一個範圍可能包含五個連續的叢集，另一個則是剩餘的25個群集。

在任何範圍的磁片上，並不保證任何其他範圍的任何關聯性。 例如，第一個範圍可能與後續的範圍在更高的 LCN。

 

 



