---
description: 針對 ASF 資料流程使用相互排除
ms.assetid: fdd31eac-1dd6-45f0-90fb-d5a74c85db2e
title: 針對 ASF 資料流程使用相互排除
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 411b5aa0638ab1c56298b93d01e8de99920abc6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977254"
---
# <a name="using-mutual-exclusion-for-asf-streams"></a>針對 ASF 資料流程使用相互排除

ASF 內容可以包含多個互斥的資料流程。 這些資料流程無法同時讀取，但是一次只能讀取其中一個。 例如，檔案可以包含一組資料流程，其中包含以不同位元速率編碼的相同內容。 使用的資料流程取決於串流內容的應用程式可用的頻寬。 ASF 相互排除物件（標頭物件的一部分）會儲存互斥資料流程群組的相關資訊。

在媒體基礎中，公開 [**IMFASFMutualExclusion**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion)介面的 *相互排除* 物件存在於每個 ASF 相互排除物件中。 設定檔物件會保存所有相互排除物件的參考。

相互排除物件會將互斥資料流程群組的相關資訊儲存為記錄。 相互排除物件可以有多個記錄，可用來建立複雜的案例。 每一筆記錄都包含一或多個資料流程，而這些資料流程無法與另一筆記錄中的資料流程並存，這取決於相互排除的類型（例如位元速率）。

複雜互斥的常見範例是檔案，其中包含三種語言的相同內容的三個音訊串流。 一次只能播放九個數據流中的其中一個，但兩個類型彼此互斥：語言和位元速率。

在此範例中，會將下列資料流程編號指派給九個串流：

<dl> 1-語言1，位速率1  
2-語言1，位速率2  
3-語言1，位速率3  
4-語言2，位速率1  
5-語言2，位速率2  
6-語言2，位速率3  
7-語言3，位速率1  
8-語言3，位速率2  
9-語言3，位速率3  
</dl>

您可以使用下列四個相互排除物件來執行此案例：

-   第一個互斥物件包括資料流程1、2和3，以位元速率互斥。 每個串流都有自己的記錄。
-   第二個相互排除物件包括資料流程4、5和6，以位元速率互斥。 每個串流都有自己的記錄。
-   第三個相互排除物件包括7、8和9，以位元速率互斥。 每個串流都有自己的記錄。
-   第四個互斥物件包含三筆記錄，第一個包括資料流程1、2和3。第二個包括串流4、5和 6;第三個包括串流7、8和9。 這些記錄會依語言相互排斥。

以這種方式建立檔案時，串流應用程式會先選取語言，因為不太可能變更在簡報的中間，然後選取位元速率。

## <a name="mutual-exclusion-object-creation-and-configuration"></a>相互排除物件的建立和設定

下列清單摘要說明設定相互排除物件的流程：

1.  建立相互排除物件。
2.  設定相互排除的類型。
3.  藉由加入記錄和相關聯的資料流程來設定相互排除物件。
4.  將相互排除物件新增至設定檔。

若要建立及設定相互排除物件

1.  呼叫 [**IMFASFProfile：： CreateMutualExclusion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createmutualexclusion) ，以建立空的互斥物件。
2.  呼叫 [**IMFASFMutualExclusion：： >advanced.field.settype**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-settype) 來設定互斥資料流程的準則。

    資料流程可以依語言、位元速率、簡報和自訂準則相互排斥。 型別會以 GUID 表示。 如需這些常數的清單，請參閱 [ASF 相互排除類型 guid](asf-mutual-exclusion-type-guids.md)。

3.  呼叫 [**IMFASFMutualExclusion：： AddRecord**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-addrecord) ，將記錄新增至相互排除物件。

    這個方法會新增空白記錄，並為其指派以零為起始的記錄索引。

4.  呼叫 [**IMFASFMutualExclusion：： AddStreamForRecord**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-addstreamforrecord) ，將資料流程號碼加入至記錄索引所指定的記錄。

    每一筆記錄都包含一或多個資料流程。 記錄中的每個資料流程都會與其他每一筆記錄中的所有資料流程相互排斥。 若要取得記錄中的資料流程數目，請指定記錄索引來呼叫 [**IMFASFMutualExclusion：： GetStreamsForRecord**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-getstreamsforrecord) 。

    若要從記錄中移除資料流程，請呼叫 [**IMFASFMutualExclusion：： RemoveStreamFromRecord**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-removestreamfromrecord) ，並指定記錄索引和資料流程號碼。

5.  呼叫 [**IMFASFProfile：： AddMutualExclusion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-addmutualexclusion) ，將設定的互斥物件新增至設定檔。

## <a name="enumerating-mutual-exclusion-objects-in-a-profile"></a>列舉設定檔中的相互排除物件

如果 [**IMFASFProfile：： AddMutualExclusion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-addmutualexclusion) 成功，它會將索引指派給指定的物件，從零開始。

若要列舉與設定檔相關聯的相互排除物件，請呼叫 [**IMFASFProfile：： GetMutualExclusionCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getmutualexclusioncount) ，並藉由呼叫 [**IMFASFProfile：： GetMutualExclusion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getmutualexclusion)，在清單中執行迴圈。 相互排除索引是連續的，範圍介於0到1之間的範圍，小於 **GetMutualExclusionCount** 抓取的資料流程數目。

呼叫 [**IMFASFProfile：： RemoveMutualExclusion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removemutualexclusion)，即可從設定檔中移除相互排除物件。 設定檔會重新指派相互排除索引，使其以零開始順序。 這會覆寫先前儲存的索引，這些索引在呼叫這個方法之後將不再有效。 這會釋放相關聯的互斥串流記錄。

## <a name="removing-records-in-a-mutual-exclusion-object"></a>移除相互排除物件中的記錄

若要從相互排除物件中移除記錄，請呼叫 [**IMFASFMutualExclusion：： RemoveRecord**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-removerecord)。 如果這個方法成功，相互排除物件會編制其餘記錄的索引，使其順序從零開始。 應用程式應該列舉記錄，以確保每一筆記錄都有正確的索引。 若要這樣做，請呼叫 [**IMFASFMutualExclusion：： GetRecordCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-getrecordcount) ，然後藉由呼叫 [**IMFASFMutualExclusion：： GetStreamsForRecord**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-getstreamsforrecord)，在記錄中執行迴圈。

移除具有最高索引的記錄不會影響其他索引。

## <a name="modifying-a-mutual-exclusion-object"></a>修改相互排除物件

若要變更設定檔中相互排除物件的設定，應用程式必須以包含新設定的另一個物件來取代現有的相互排除物件。

變更設定檔中相互排除物件的設定

1.  列舉設定檔中的相互排除物件，以取得需要變更的物件。
2.  呼叫 [**IMFASFMutualExclusion：： clone**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-clone) 以複製相互排除物件。

3.  視需要設定複製的物件。
4.  呼叫 [**IMFASFProfile：： RemoveMutualExclusion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removemutualexclusion) ，從設定檔中移除舊的相互排除物件。

5.  呼叫 [**IMFASFProfile：： AddMutualExclusion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-addmutualexclusion) ，將更新的相互排除物件新增至設定檔。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ASF 設定檔](asf-profile.md)
</dt> </dl>

 

 



