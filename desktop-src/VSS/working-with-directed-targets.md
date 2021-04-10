---
description: 導向的目的機制可讓寫入器在還原時重新對應檔案。
ms.assetid: c0b4ab26-2bb6-4b0f-b837-01057983b49b
title: 使用導向的目標
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bd2e15ec873b87030a2d01be69d2c3e5f95a193
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026232"
---
# <a name="working-with-directed-targets"></a>使用導向的目標

[*導向的目標*](vssgloss-d.md)機制可讓寫入器在還原時重新對應檔案。 這可讓寫入器執行下列動作：

-   指定新的目標位置 (類似于要求者的 [**>ivssbackupcomponents：： AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget)) 。
-   藉由只將檔案的必要部分還原至磁片來回收磁碟空間，特別是在使用 [*部分*](vssgloss-p.md) 檔案機制來備份檔案時。
-   變更檔案格式以符合目前的需求。

任何要與導向的目標作業搭配使用的檔案，都必須有 VSS RT 導向的 [*還原目標*](vssgloss-r.md) \_ \_ 。

一旦建立了要求者可以支援導向的目標作業之後，寫入器 (處理 [**PreRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore)事件時) 會針對 [**>ivsscomponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)的實例使用 [**>ivsscomponent：： AddDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddirectedtarget) ，該實例對應于管理檔案的元件 (或定義包含檔案的元件集) 定義檔案在還原時重新對應的方式。

在使用 [**>ivsscomponent：： AddDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddirectedtarget)中，寫入器會指定用來備份檔案的檔案名和路徑、其還原目的地的檔案名和路徑 (這些值可以與原始檔案名和路徑) ，以及來源和目的地檔案範圍相同。

如同部分檔案作業，範圍清單是要 (備份到檔案中的位移組（以位元組為單位）) 和要還原的區段長度 (（以位元組為單位）) 、以冒號分隔的位移和長度，以及每一組以逗號分隔： *Offset1 ***：**_array2d.length1_*_，_* * Offset2 ***：**_array3d.length2_。 每個值都是十六進位或十進位格式的64位整數。

如果寫入器需要使用導向的目的機制讓要求者將檔案還原至新的位置，它就會呼叫 [**>ivsscomponent：： AddDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddirectedtarget) ，其中包含原始的檔案名和路徑以及新的檔案名和路徑，並以零位移和長度等於整個檔案大小的長度來指定來源目的地範圍。

比方說，如果寫入器需要200K 檔案（C： \\ WriterData \\ Index），並還原為 c： \\ WriterData \\ OldIndex，則來源和目的地範圍字串會是 "**0:204880**"。

若要重新對應大型的部份備份檔，要求者會使用用來備份檔案的來源範圍，以及將會減少檔案大小的目的範圍。 您可以使用 [**>ivsscomponent：： GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile) 來取得來源範圍資訊，該實例對應至管理檔案 [**(的元件**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) ，或可定義包含檔案) 之元件集的元件。

如果部份備份的檔案一開始是一個大型檔案，其標頭為位元組64-512、包含記錄計數和其他經常更新的資訊，而且最新的資料是在檔案的最後65536個位元組中找到（0x1239E8577A 至0x1239E7577A 的位元組），寫入器可以將來源範圍清單指定為字串 "**64：448，0x1239E8577A： 65536**"。

如果寫入器想要重新對應已還原的檔案，只包含標頭和最新的資料，則範圍清單可以是 "**0：488488： 65536**" 字串。

在實際執行還原作業之前，要求者應該檢查是否有任何檔案需要導向的目標支援。

若要這樣做，要求者會先使用 [**>ivssbackupcomponents：： GetWriterComponentsCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponentscount) 和 [**>ivssbackupcomponents：： GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents)，在其備份元件檔中逐一查看具有預存元件的寫入器。

然後， [**>ivssbackupcomponents：： GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents) 介面會用來傳回 [**IVssWriterComponentsExt**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) 介面的實例，其提供 [**IVssWriterComponentsExt：： GetComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponent) 和 [**IVssWriterComponentsExt：： GetComponentCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponentcount) 方法，可讓要求者取得 [**>ivsscomponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) 實例。

這可讓要求者使用 [**>ivsscomponent：： GetDirectedTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtargetcount) 和 [**>ivsscomponent：： GetDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtarget) 來取得導向的目標 [**候選項，**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) 該實例會對應至管理檔案 (的元件，或是定義包含檔案) 之元件集的元件。

 

 
