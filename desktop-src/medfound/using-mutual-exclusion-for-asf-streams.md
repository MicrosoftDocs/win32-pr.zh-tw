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
# <a name="using-mutual-exclusion-for-asf-streams"></a><span data-ttu-id="3b41b-103">針對 ASF 資料流程使用相互排除</span><span class="sxs-lookup"><span data-stu-id="3b41b-103">Using Mutual Exclusion for ASF Streams</span></span>

<span data-ttu-id="3b41b-104">ASF 內容可以包含多個互斥的資料流程。</span><span class="sxs-lookup"><span data-stu-id="3b41b-104">ASF content can contain multiple streams that are mutually exclusive.</span></span> <span data-ttu-id="3b41b-105">這些資料流程無法同時讀取，但是一次只能讀取其中一個。</span><span class="sxs-lookup"><span data-stu-id="3b41b-105">These streams cannot be read concurrently but only one of them is read at a time.</span></span> <span data-ttu-id="3b41b-106">例如，檔案可以包含一組資料流程，其中包含以不同位元速率編碼的相同內容。</span><span class="sxs-lookup"><span data-stu-id="3b41b-106">For example, the file can contain a set of streams that includes the same content encoded at a different bit rate.</span></span> <span data-ttu-id="3b41b-107">使用的資料流程取決於串流內容的應用程式可用的頻寬。</span><span class="sxs-lookup"><span data-stu-id="3b41b-107">The stream that is used is determined by the bandwidth available to the application that streams the content.</span></span> <span data-ttu-id="3b41b-108">ASF 相互排除物件（標頭物件的一部分）會儲存互斥資料流程群組的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3b41b-108">The ASF Mutual Exclusion Object, which is part of the Header Object, stores information about the group of mutually exclusive streams.</span></span>

<span data-ttu-id="3b41b-109">在媒體基礎中，公開 [**IMFASFMutualExclusion**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion)介面的 *相互排除* 物件存在於每個 ASF 相互排除物件中。</span><span class="sxs-lookup"><span data-stu-id="3b41b-109">In Media Foundation, the *mutual exclusion* object that exposes the [**IMFASFMutualExclusion**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion) interface exists for every ASF Mutual Exclusion Object.</span></span> <span data-ttu-id="3b41b-110">設定檔物件會保存所有相互排除物件的參考。</span><span class="sxs-lookup"><span data-stu-id="3b41b-110">The profile object holds reference to all mutual exclusion objects.</span></span>

<span data-ttu-id="3b41b-111">相互排除物件會將互斥資料流程群組的相關資訊儲存為記錄。</span><span class="sxs-lookup"><span data-stu-id="3b41b-111">The mutual exclusion object stores information about the group of mutually exclusive streams as records.</span></span> <span data-ttu-id="3b41b-112">相互排除物件可以有多個記錄，可用來建立複雜的案例。</span><span class="sxs-lookup"><span data-stu-id="3b41b-112">A mutual exclusion object can have multiple records that can be used to create complex scenarios.</span></span> <span data-ttu-id="3b41b-113">每一筆記錄都包含一或多個資料流程，而這些資料流程無法與另一筆記錄中的資料流程並存，這取決於相互排除的類型（例如位元速率）。</span><span class="sxs-lookup"><span data-stu-id="3b41b-113">Each record contains one or more streams that cannot coexist with streams in another record, maintained by the mutual exclusion object, depending on the type of mutual exclusion, such as bit rate.</span></span>

<span data-ttu-id="3b41b-114">複雜互斥的常見範例是檔案，其中包含三種語言的相同內容的三個音訊串流。</span><span class="sxs-lookup"><span data-stu-id="3b41b-114">A common example of complex mutual exclusion is a file that contains three audio streams of the same content at various bit rates in each of three languages.</span></span> <span data-ttu-id="3b41b-115">一次只能播放九個數據流中的其中一個，但兩個類型彼此互斥：語言和位元速率。</span><span class="sxs-lookup"><span data-stu-id="3b41b-115">Only one of the nine streams should be played at a time, but there are two types by which they are mutually exclusive: language and bit rate.</span></span>

<span data-ttu-id="3b41b-116">在此範例中，會將下列資料流程編號指派給九個串流：</span><span class="sxs-lookup"><span data-stu-id="3b41b-116">For this example, the nine streams are assigned the following stream numbers:</span></span>

<dl> <span data-ttu-id="3b41b-117">1-語言1，位速率1</span><span class="sxs-lookup"><span data-stu-id="3b41b-117">1 - Language 1, bit rate 1</span></span>  
<span data-ttu-id="3b41b-118">2-語言1，位速率2</span><span class="sxs-lookup"><span data-stu-id="3b41b-118">2 - Language 1, bit rate 2</span></span>  
<span data-ttu-id="3b41b-119">3-語言1，位速率3</span><span class="sxs-lookup"><span data-stu-id="3b41b-119">3 - Language 1, bit rate 3</span></span>  
<span data-ttu-id="3b41b-120">4-語言2，位速率1</span><span class="sxs-lookup"><span data-stu-id="3b41b-120">4 - Language 2, bit rate 1</span></span>  
<span data-ttu-id="3b41b-121">5-語言2，位速率2</span><span class="sxs-lookup"><span data-stu-id="3b41b-121">5 - Language 2, bit rate 2</span></span>  
<span data-ttu-id="3b41b-122">6-語言2，位速率3</span><span class="sxs-lookup"><span data-stu-id="3b41b-122">6 - Language 2, bit rate 3</span></span>  
<span data-ttu-id="3b41b-123">7-語言3，位速率1</span><span class="sxs-lookup"><span data-stu-id="3b41b-123">7 - Language 3, bit rate 1</span></span>  
<span data-ttu-id="3b41b-124">8-語言3，位速率2</span><span class="sxs-lookup"><span data-stu-id="3b41b-124">8 - Language 3, bit rate 2</span></span>  
<span data-ttu-id="3b41b-125">9-語言3，位速率3</span><span class="sxs-lookup"><span data-stu-id="3b41b-125">9 - Language 3, bit rate 3</span></span>  
</dl>

<span data-ttu-id="3b41b-126">您可以使用下列四個相互排除物件來執行此案例：</span><span class="sxs-lookup"><span data-stu-id="3b41b-126">This scenario can be implemented by using the following four mutual exclusion objects:</span></span>

-   <span data-ttu-id="3b41b-127">第一個互斥物件包括資料流程1、2和3，以位元速率互斥。</span><span class="sxs-lookup"><span data-stu-id="3b41b-127">The first mutual exclusion object includes streams 1, 2, and 3, mutually exclusive by bit rate.</span></span> <span data-ttu-id="3b41b-128">每個串流都有自己的記錄。</span><span class="sxs-lookup"><span data-stu-id="3b41b-128">Each stream has its own record.</span></span>
-   <span data-ttu-id="3b41b-129">第二個相互排除物件包括資料流程4、5和6，以位元速率互斥。</span><span class="sxs-lookup"><span data-stu-id="3b41b-129">The second mutual exclusion object includes streams 4, 5, and 6, mutually exclusive by bit rate.</span></span> <span data-ttu-id="3b41b-130">每個串流都有自己的記錄。</span><span class="sxs-lookup"><span data-stu-id="3b41b-130">Each stream has its own record.</span></span>
-   <span data-ttu-id="3b41b-131">第三個相互排除物件包括7、8和9，以位元速率互斥。</span><span class="sxs-lookup"><span data-stu-id="3b41b-131">The third mutual exclusion object includes 7, 8, and 9, mutually exclusive by bit rate.</span></span> <span data-ttu-id="3b41b-132">每個串流都有自己的記錄。</span><span class="sxs-lookup"><span data-stu-id="3b41b-132">Each stream has its own record.</span></span>
-   <span data-ttu-id="3b41b-133">第四個互斥物件包含三筆記錄，第一個包括資料流程1、2和3。第二個包括串流4、5和 6;第三個包括串流7、8和9。</span><span class="sxs-lookup"><span data-stu-id="3b41b-133">The fourth mutual exclusion object contains three records, the first including streams 1, 2, and 3; the second including streams 4, 5, and 6; and the third including streams 7, 8, and 9.</span></span> <span data-ttu-id="3b41b-134">這些記錄會依語言相互排斥。</span><span class="sxs-lookup"><span data-stu-id="3b41b-134">These records are mutually exclusive by language.</span></span>

<span data-ttu-id="3b41b-135">以這種方式建立檔案時，串流應用程式會先選取語言，因為不太可能變更在簡報的中間，然後選取位元速率。</span><span class="sxs-lookup"><span data-stu-id="3b41b-135">When playing a file created in this way, the streaming application selects the language first because it is less likely to change in the middle of presentation and then selects a bit rate.</span></span>

## <a name="mutual-exclusion-object-creation-and-configuration"></a><span data-ttu-id="3b41b-136">相互排除物件的建立和設定</span><span class="sxs-lookup"><span data-stu-id="3b41b-136">Mutual Exclusion Object Creation and Configuration</span></span>

<span data-ttu-id="3b41b-137">下列清單摘要說明設定相互排除物件的流程：</span><span class="sxs-lookup"><span data-stu-id="3b41b-137">The following list summarizes the process of configuring a mutual exclusion object:</span></span>

1.  <span data-ttu-id="3b41b-138">建立相互排除物件。</span><span class="sxs-lookup"><span data-stu-id="3b41b-138">Create a mutual exclusion object.</span></span>
2.  <span data-ttu-id="3b41b-139">設定相互排除的類型。</span><span class="sxs-lookup"><span data-stu-id="3b41b-139">Set the type of mutual exclusion.</span></span>
3.  <span data-ttu-id="3b41b-140">藉由加入記錄和相關聯的資料流程來設定相互排除物件。</span><span class="sxs-lookup"><span data-stu-id="3b41b-140">Configure the mutual exclusion object by adding records and the associated streams.</span></span>
4.  <span data-ttu-id="3b41b-141">將相互排除物件新增至設定檔。</span><span class="sxs-lookup"><span data-stu-id="3b41b-141">Add the mutual exclusion object to the profile.</span></span>

<span data-ttu-id="3b41b-142">若要建立及設定相互排除物件</span><span class="sxs-lookup"><span data-stu-id="3b41b-142">To create and configure a mutual exclusion object</span></span>

1.  <span data-ttu-id="3b41b-143">呼叫 [**IMFASFProfile：： CreateMutualExclusion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createmutualexclusion) ，以建立空的互斥物件。</span><span class="sxs-lookup"><span data-stu-id="3b41b-143">Call [**IMFASFProfile::CreateMutualExclusion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createmutualexclusion) to create an empty mutual exclusion object.</span></span>
2.  <span data-ttu-id="3b41b-144">呼叫 [**IMFASFMutualExclusion：： >advanced.field.settype**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-settype) 來設定互斥資料流程的準則。</span><span class="sxs-lookup"><span data-stu-id="3b41b-144">Call [**IMFASFMutualExclusion::SetType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-settype) to set the criterion of the mutually exclusive stream.</span></span>

    <span data-ttu-id="3b41b-145">資料流程可以依語言、位元速率、簡報和自訂準則相互排斥。</span><span class="sxs-lookup"><span data-stu-id="3b41b-145">The streams can be mutually exclusive by language, bit rate, presentation, and custom criteria.</span></span> <span data-ttu-id="3b41b-146">型別會以 GUID 表示。</span><span class="sxs-lookup"><span data-stu-id="3b41b-146">The type is represented as a GUID.</span></span> <span data-ttu-id="3b41b-147">如需這些常數的清單，請參閱 [ASF 相互排除類型 guid](asf-mutual-exclusion-type-guids.md)。</span><span class="sxs-lookup"><span data-stu-id="3b41b-147">For a list of these constants, see [ASF Mutual Exclusion Type GUIDs](asf-mutual-exclusion-type-guids.md).</span></span>

3.  <span data-ttu-id="3b41b-148">呼叫 [**IMFASFMutualExclusion：： AddRecord**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-addrecord) ，將記錄新增至相互排除物件。</span><span class="sxs-lookup"><span data-stu-id="3b41b-148">Call [**IMFASFMutualExclusion::AddRecord**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-addrecord) to add a record to the mutual exclusion object.</span></span>

    <span data-ttu-id="3b41b-149">這個方法會新增空白記錄，並為其指派以零為起始的記錄索引。</span><span class="sxs-lookup"><span data-stu-id="3b41b-149">This method adds an empty record and assigns it a record index starting with zero.</span></span>

4.  <span data-ttu-id="3b41b-150">呼叫 [**IMFASFMutualExclusion：： AddStreamForRecord**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-addstreamforrecord) ，將資料流程號碼加入至記錄索引所指定的記錄。</span><span class="sxs-lookup"><span data-stu-id="3b41b-150">Call [**IMFASFMutualExclusion::AddStreamForRecord**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-addstreamforrecord) to add the stream number to the record specified by the record index.</span></span>

    <span data-ttu-id="3b41b-151">每一筆記錄都包含一或多個資料流程。</span><span class="sxs-lookup"><span data-stu-id="3b41b-151">Each record includes one or more streams.</span></span> <span data-ttu-id="3b41b-152">記錄中的每個資料流程都會與其他每一筆記錄中的所有資料流程相互排斥。</span><span class="sxs-lookup"><span data-stu-id="3b41b-152">Every stream in a record is mutually exclusive of all streams in every other record.</span></span> <span data-ttu-id="3b41b-153">若要取得記錄中的資料流程數目，請指定記錄索引來呼叫 [**IMFASFMutualExclusion：： GetStreamsForRecord**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-getstreamsforrecord) 。</span><span class="sxs-lookup"><span data-stu-id="3b41b-153">To get the number of streams in a record, call [**IMFASFMutualExclusion::GetStreamsForRecord**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-getstreamsforrecord) by specifying the record index.</span></span>

    <span data-ttu-id="3b41b-154">若要從記錄中移除資料流程，請呼叫 [**IMFASFMutualExclusion：： RemoveStreamFromRecord**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-removestreamfromrecord) ，並指定記錄索引和資料流程號碼。</span><span class="sxs-lookup"><span data-stu-id="3b41b-154">To remove a stream from the record, call [**IMFASFMutualExclusion::RemoveStreamFromRecord**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-removestreamfromrecord) and specify the record index and the stream number.</span></span>

5.  <span data-ttu-id="3b41b-155">呼叫 [**IMFASFProfile：： AddMutualExclusion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-addmutualexclusion) ，將設定的互斥物件新增至設定檔。</span><span class="sxs-lookup"><span data-stu-id="3b41b-155">Call [**IMFASFProfile::AddMutualExclusion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-addmutualexclusion) to add the configured mutual exclusion object to the profile.</span></span>

## <a name="enumerating-mutual-exclusion-objects-in-a-profile"></a><span data-ttu-id="3b41b-156">列舉設定檔中的相互排除物件</span><span class="sxs-lookup"><span data-stu-id="3b41b-156">Enumerating Mutual Exclusion Objects in a Profile</span></span>

<span data-ttu-id="3b41b-157">如果 [**IMFASFProfile：： AddMutualExclusion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-addmutualexclusion) 成功，它會將索引指派給指定的物件，從零開始。</span><span class="sxs-lookup"><span data-stu-id="3b41b-157">If [**IMFASFProfile::AddMutualExclusion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-addmutualexclusion) succeeds, it assigns an index to the specified object, starting at zero.</span></span>

<span data-ttu-id="3b41b-158">若要列舉與設定檔相關聯的相互排除物件，請呼叫 [**IMFASFProfile：： GetMutualExclusionCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getmutualexclusioncount) ，並藉由呼叫 [**IMFASFProfile：： GetMutualExclusion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getmutualexclusion)，在清單中執行迴圈。</span><span class="sxs-lookup"><span data-stu-id="3b41b-158">To enumerate the mutual exclusion objects associated with a profile, call [**IMFASFProfile::GetMutualExclusionCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getmutualexclusioncount) and loop through the list by calling [**IMFASFProfile::GetMutualExclusion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getmutualexclusion).</span></span> <span data-ttu-id="3b41b-159">相互排除索引是連續的，範圍介於0到1之間的範圍，小於 **GetMutualExclusionCount** 抓取的資料流程數目。</span><span class="sxs-lookup"><span data-stu-id="3b41b-159">Mutual exclusion indexes are sequential and range between 0 and one less than the number of streams retrieved by **GetMutualExclusionCount**.</span></span>

<span data-ttu-id="3b41b-160">呼叫 [**IMFASFProfile：： RemoveMutualExclusion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removemutualexclusion)，即可從設定檔中移除相互排除物件。</span><span class="sxs-lookup"><span data-stu-id="3b41b-160">A mutual exclusion object is removed from the profile by calling [**IMFASFProfile::RemoveMutualExclusion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removemutualexclusion).</span></span> <span data-ttu-id="3b41b-161">設定檔會重新指派相互排除索引，使其以零開始順序。</span><span class="sxs-lookup"><span data-stu-id="3b41b-161">The profile reassigns the mutual exclusion indexes so that they are sequential starting with zero.</span></span> <span data-ttu-id="3b41b-162">這會覆寫先前儲存的索引，這些索引在呼叫這個方法之後將不再有效。</span><span class="sxs-lookup"><span data-stu-id="3b41b-162">This overwrites previously stored indexes, which are no longer valid after calling this method.</span></span> <span data-ttu-id="3b41b-163">這會釋放相關聯的互斥串流記錄。</span><span class="sxs-lookup"><span data-stu-id="3b41b-163">This releases the associated mutual exclusion stream records.</span></span>

## <a name="removing-records-in-a-mutual-exclusion-object"></a><span data-ttu-id="3b41b-164">移除相互排除物件中的記錄</span><span class="sxs-lookup"><span data-stu-id="3b41b-164">Removing Records in a Mutual Exclusion Object</span></span>

<span data-ttu-id="3b41b-165">若要從相互排除物件中移除記錄，請呼叫 [**IMFASFMutualExclusion：： RemoveRecord**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-removerecord)。</span><span class="sxs-lookup"><span data-stu-id="3b41b-165">To remove a record from a mutual exclusion object, call [**IMFASFMutualExclusion::RemoveRecord**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-removerecord).</span></span> <span data-ttu-id="3b41b-166">如果這個方法成功，相互排除物件會編制其餘記錄的索引，使其順序從零開始。</span><span class="sxs-lookup"><span data-stu-id="3b41b-166">If this method succeeds, the mutual exclusion object indexes the remaining records so that they are sequential starting with zero.</span></span> <span data-ttu-id="3b41b-167">應用程式應該列舉記錄，以確保每一筆記錄都有正確的索引。</span><span class="sxs-lookup"><span data-stu-id="3b41b-167">The application should enumerate the records to ensure the correct index for each record.</span></span> <span data-ttu-id="3b41b-168">若要這樣做，請呼叫 [**IMFASFMutualExclusion：： GetRecordCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-getrecordcount) ，然後藉由呼叫 [**IMFASFMutualExclusion：： GetStreamsForRecord**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-getstreamsforrecord)，在記錄中執行迴圈。</span><span class="sxs-lookup"><span data-stu-id="3b41b-168">To do so, call [**IMFASFMutualExclusion::GetRecordCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-getrecordcount) and loop through the records by calling [**IMFASFMutualExclusion::GetStreamsForRecord**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-getstreamsforrecord).</span></span>

<span data-ttu-id="3b41b-169">移除具有最高索引的記錄不會影響其他索引。</span><span class="sxs-lookup"><span data-stu-id="3b41b-169">Removing the record with the highest index has no effect on the other indexes.</span></span>

## <a name="modifying-a-mutual-exclusion-object"></a><span data-ttu-id="3b41b-170">修改相互排除物件</span><span class="sxs-lookup"><span data-stu-id="3b41b-170">Modifying a Mutual Exclusion Object</span></span>

<span data-ttu-id="3b41b-171">若要變更設定檔中相互排除物件的設定，應用程式必須以包含新設定的另一個物件來取代現有的相互排除物件。</span><span class="sxs-lookup"><span data-stu-id="3b41b-171">To change the configuration of the mutual exclusion object in the profile, the application must replace the existing mutual exclusion object with another object that contains the new settings.</span></span>

<span data-ttu-id="3b41b-172">變更設定檔中相互排除物件的設定</span><span class="sxs-lookup"><span data-stu-id="3b41b-172">To change the configuration of the mutual exclusion object in the profile</span></span>

1.  <span data-ttu-id="3b41b-173">列舉設定檔中的相互排除物件，以取得需要變更的物件。</span><span class="sxs-lookup"><span data-stu-id="3b41b-173">Enumerate the mutual exclusion objects in the profile to get the object that needs to be changed.</span></span>
2.  <span data-ttu-id="3b41b-174">呼叫 [**IMFASFMutualExclusion：： clone**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-clone) 以複製相互排除物件。</span><span class="sxs-lookup"><span data-stu-id="3b41b-174">Call [**IMFASFMutualExclusion::Clone**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-clone) to clone the mutual exclusion object.</span></span>

3.  <span data-ttu-id="3b41b-175">視需要設定複製的物件。</span><span class="sxs-lookup"><span data-stu-id="3b41b-175">Configure the cloned object as required.</span></span>
4.  <span data-ttu-id="3b41b-176">呼叫 [**IMFASFProfile：： RemoveMutualExclusion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removemutualexclusion) ，從設定檔中移除舊的相互排除物件。</span><span class="sxs-lookup"><span data-stu-id="3b41b-176">Call [**IMFASFProfile::RemoveMutualExclusion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removemutualexclusion) to remove the old mutual exclusion object from the profile.</span></span>

5.  <span data-ttu-id="3b41b-177">呼叫 [**IMFASFProfile：： AddMutualExclusion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-addmutualexclusion) ，將更新的相互排除物件新增至設定檔。</span><span class="sxs-lookup"><span data-stu-id="3b41b-177">Call [**IMFASFProfile::AddMutualExclusion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-addmutualexclusion) to add the updated mutual exclusion object to the profile.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3b41b-178">相關主題</span><span class="sxs-lookup"><span data-stu-id="3b41b-178">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b41b-179">ASF 設定檔</span><span class="sxs-lookup"><span data-stu-id="3b41b-179">ASF Profile</span></span>](asf-profile.md)
</dt> </dl>

 

 



