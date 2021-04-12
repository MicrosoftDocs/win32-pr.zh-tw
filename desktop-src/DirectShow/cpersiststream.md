---
description: CPersistStream 是篩選的持續性屬性基類 (也就是，在儲存的圖形) 中篩選屬性。
ms.assetid: 8073e2be-aaf9-4b01-a7d5-bab5c1dcc19b
title: CPersistStream 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream
api_type:
- COM
api_location: ''
ms.openlocfilehash: 690a0f45fab7c3612d215a859798460abc81728e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104509857"
---
# <a name="cpersiststream-class"></a><span data-ttu-id="d873e-103">CPersistStream 類別</span><span class="sxs-lookup"><span data-stu-id="d873e-103">CPersistStream class</span></span>

![cpersiststream 類別階層](images/pstrm01.png)

<span data-ttu-id="d873e-105">`CPersistStream` 是篩選的持續性屬性的基類 (也就是，在儲存的圖形) 中篩選屬性。</span><span class="sxs-lookup"><span data-stu-id="d873e-105">`CPersistStream` is the base class for persistent properties of filters (that is, filter properties in saved graphs).</span></span>

<span data-ttu-id="d873e-106">最簡單的使用方式 `CPersistStream` 是：</span><span class="sxs-lookup"><span data-stu-id="d873e-106">The simplest way to use `CPersistStream` is to:</span></span>

1.  <span data-ttu-id="d873e-107">排列篩選準則，以繼承這個類別。</span><span class="sxs-lookup"><span data-stu-id="d873e-107">Arrange for your filter to inherit this class.</span></span>
2.  <span data-ttu-id="d873e-108">在您的類別中執行 [**WriteToStream**](cpersiststream-writetostream.md) 和 [**ReadFromStream**](cpersiststream-readfromstream.md) 。</span><span class="sxs-lookup"><span data-stu-id="d873e-108">Implement [**WriteToStream**](cpersiststream-writetostream.md) and [**ReadFromStream**](cpersiststream-readfromstream.md) in your class.</span></span> <span data-ttu-id="d873e-109">這些函式會覆寫此處的函式，而不執行任何動作，而是做為預留位置。</span><span class="sxs-lookup"><span data-stu-id="d873e-109">These will override the functions here, which do nothing but act as placeholders.</span></span>
3.  <span data-ttu-id="d873e-110">變更您的 **NonDelegatingQueryInterface** 以處理 **IPersistStream**。</span><span class="sxs-lookup"><span data-stu-id="d873e-110">Change your **NonDelegatingQueryInterface** to handle **IPersistStream**.</span></span>
4.  <span data-ttu-id="d873e-111">執行 [**SizeMax**](cpersiststream-sizemax.md) ，以傳回您儲存的資料位元組數上限。</span><span class="sxs-lookup"><span data-stu-id="d873e-111">Implement [**SizeMax**](cpersiststream-sizemax.md) to return an upper bound on the number of bytes of data you save.</span></span>

    <span data-ttu-id="d873e-112">如果您儲存 Unicode™資料，請記住 WCHAR 是2個位元組。</span><span class="sxs-lookup"><span data-stu-id="d873e-112">If you save Unicode™ data, remember that a WCHAR is 2 bytes.</span></span>

5.  <span data-ttu-id="d873e-113">當您的資料變更時，請呼叫 [**SetDirty**](cpersiststream-setdirty.md)。</span><span class="sxs-lookup"><span data-stu-id="d873e-113">When your data changes, call [**SetDirty**](cpersiststream-setdirty.md).</span></span>

## <a name="version-numbers"></a><span data-ttu-id="d873e-114">版本號碼</span><span class="sxs-lookup"><span data-stu-id="d873e-114">Version Numbers</span></span>

<span data-ttu-id="d873e-115">在某個時間點，您可能會決定改變或擴充資料的格式。</span><span class="sxs-lookup"><span data-stu-id="d873e-115">At some point you might decide to alter or extend the format of your data.</span></span> <span data-ttu-id="d873e-116">然後，您會希望所有舊儲存的串流中都有一個版本號碼，如此您就可以在讀取它們時告訴您，是否代表舊的或新的表單。</span><span class="sxs-lookup"><span data-stu-id="d873e-116">You will then wish you had a version number in all the old saved streams so you can tell, when you read them, whether they represent the old or new form.</span></span> <span data-ttu-id="d873e-117">為了協助您，這個類別會寫入和讀取版本號碼。</span><span class="sxs-lookup"><span data-stu-id="d873e-117">To assist you, this class writes and reads a version number.</span></span> <span data-ttu-id="d873e-118">寫入時，它會呼叫 [**GetSoftwareVersion**](cpersiststream-getsoftwareversion.md) 來查詢目前正在使用的軟體版本。</span><span class="sxs-lookup"><span data-stu-id="d873e-118">When it writes, it calls [**GetSoftwareVersion**](cpersiststream-getsoftwareversion.md) to inquire as to the version of the software being used at the moment.</span></span> <span data-ttu-id="d873e-119"> (實際上是檔案中資料配置的版本號碼。 ) 它會將此資料寫入資料中的第一件事。</span><span class="sxs-lookup"><span data-stu-id="d873e-119">(In effect, this is a version number of the data layout in the file.) It writes this as the first thing in the data.</span></span> <span data-ttu-id="d873e-120">如果您想要變更版本，請執行 (覆寫) **GetSoftwareVersion**。</span><span class="sxs-lookup"><span data-stu-id="d873e-120">If you want to change the version, implement (override) **GetSoftwareVersion**.</span></span> <span data-ttu-id="d873e-121">它會先將檔案中的版本號碼 **讀入 \_ mp dwFileVersion** ，然後再呼叫 [**ReadFromStream**](cpersiststream-readfromstream.md)，因此在 **ReadFromStream** 中，您可以檢查 **mp \_ dwFileVersion** 以查看是否正在讀取舊的版本檔案。</span><span class="sxs-lookup"><span data-stu-id="d873e-121">It reads the version number from the file into **mPS\_dwFileVersion** before calling [**ReadFromStream**](cpersiststream-readfromstream.md), so in **ReadFromStream** you can check **mPS\_dwFileVersion** to see if you are reading an old version file.</span></span> <span data-ttu-id="d873e-122">通常，您應該接受版本比讀取的軟體版本還新的檔案。</span><span class="sxs-lookup"><span data-stu-id="d873e-122">Usually you should accept files whose version is no newer than the software version that is reading them.</span></span>

<span data-ttu-id="d873e-123">**CPersistStream** 會實施 [**IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream)。</span><span class="sxs-lookup"><span data-stu-id="d873e-123">**CPersistStream** implements [**IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream).</span></span> <span data-ttu-id="d873e-124">如需更多的執行資訊，請參閱 Microsoft Platform SDK 中的 COM 參考。</span><span class="sxs-lookup"><span data-stu-id="d873e-124">For more implementation information, see the COM Reference in the Microsoft Platform SDK.</span></span>



| <span data-ttu-id="d873e-125">受保護的資料成員</span><span class="sxs-lookup"><span data-stu-id="d873e-125">Protected Data Members</span></span>                                          | <span data-ttu-id="d873e-126">Description</span><span class="sxs-lookup"><span data-stu-id="d873e-126">Description</span></span>                                                                   |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="d873e-127">Mp \_ dwFileVersion</span><span class="sxs-lookup"><span data-stu-id="d873e-127">mPS\_dwFileVersion</span></span>                                              | <span data-ttu-id="d873e-128">檔案的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="d873e-128">Version number of the file.</span></span>                                                   |
| <span data-ttu-id="d873e-129">Mp \_ fDirty</span><span class="sxs-lookup"><span data-stu-id="d873e-129">mPS\_fDirty</span></span>                                                     | <span data-ttu-id="d873e-130">必須儲存此資料流程的資料。</span><span class="sxs-lookup"><span data-stu-id="d873e-130">Data for this stream must be saved.</span></span>                                           |
| <span data-ttu-id="d873e-131">成員函數</span><span class="sxs-lookup"><span data-stu-id="d873e-131">Member Functions</span></span>                                                | <span data-ttu-id="d873e-132">Description</span><span class="sxs-lookup"><span data-stu-id="d873e-132">Description</span></span>                                                                   |
| [<span data-ttu-id="d873e-133">**CPersistStream**</span><span class="sxs-lookup"><span data-stu-id="d873e-133">**CPersistStream**</span></span>](cpersiststream-cpersiststream.md)         | <span data-ttu-id="d873e-134">結構 **CPersistStream** 物件。</span><span class="sxs-lookup"><span data-stu-id="d873e-134">Constructs a **CPersistStream** object.</span></span>                                       |
| [<span data-ttu-id="d873e-135">**SetDirty**</span><span class="sxs-lookup"><span data-stu-id="d873e-135">**SetDirty**</span></span>](cpersiststream-setdirty.md)                     | <span data-ttu-id="d873e-136">表示必須將物件儲存至資料流程。</span><span class="sxs-lookup"><span data-stu-id="d873e-136">Indicates that the object must be saved to the stream.</span></span>                        |
| <span data-ttu-id="d873e-137">可覆寫的成員函式</span><span class="sxs-lookup"><span data-stu-id="d873e-137">Overridable Member Functions</span></span>                                    | <span data-ttu-id="d873e-138">Description</span><span class="sxs-lookup"><span data-stu-id="d873e-138">Description</span></span>                                                                   |
| [<span data-ttu-id="d873e-139">**GetClassID**</span><span class="sxs-lookup"><span data-stu-id="d873e-139">**GetClassID**</span></span>](cpersiststream-getclassid.md)                 | <span data-ttu-id="d873e-140">捕獲此資料流程的類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="d873e-140">Retrieves the class identifier of this stream.</span></span>                                |
| [<span data-ttu-id="d873e-141">**GetSoftwareVersion**</span><span class="sxs-lookup"><span data-stu-id="d873e-141">**GetSoftwareVersion**</span></span>](cpersiststream-getsoftwareversion.md) | <span data-ttu-id="d873e-142">抓取此檔案格式的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="d873e-142">Retrieves the version number for this file format.</span></span>                            |
| [<span data-ttu-id="d873e-143">**ReadFromStream**</span><span class="sxs-lookup"><span data-stu-id="d873e-143">**ReadFromStream**</span></span>](cpersiststream-readfromstream.md)         | <span data-ttu-id="d873e-144">從資料流程讀取篩選的資料。</span><span class="sxs-lookup"><span data-stu-id="d873e-144">Reads the filter's data from the stream.</span></span>                                      |
| [<span data-ttu-id="d873e-145">**SizeMax**</span><span class="sxs-lookup"><span data-stu-id="d873e-145">**SizeMax**</span></span>](cpersiststream-sizemax.md)                       | <span data-ttu-id="d873e-146">抓取資料 (不包括) 的版本號碼所需的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="d873e-146">Retrieves the number of bytes needed for data (not including version number).</span></span> |
| [<span data-ttu-id="d873e-147">**WriteToStream**</span><span class="sxs-lookup"><span data-stu-id="d873e-147">**WriteToStream**</span></span>](cpersiststream-writetostream.md)           | <span data-ttu-id="d873e-148">將篩選的資料寫入至資料流程。</span><span class="sxs-lookup"><span data-stu-id="d873e-148">Writes the filter's data to the stream.</span></span>                                       |
| <span data-ttu-id="d873e-149">IPersistStream 方法</span><span class="sxs-lookup"><span data-stu-id="d873e-149">IPersistStream Methods</span></span>                                          | <span data-ttu-id="d873e-150">Description</span><span class="sxs-lookup"><span data-stu-id="d873e-150">Description</span></span>                                                                   |
| [<span data-ttu-id="d873e-151">**GetSizeMax**</span><span class="sxs-lookup"><span data-stu-id="d873e-151">**GetSizeMax**</span></span>](cpersiststream-getsizemax.md)                 | <span data-ttu-id="d873e-152">抓取資料 (所需的位元組數目，包括) 的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="d873e-152">Retrieves the number of bytes needed for data (including version number).</span></span>     |
| [<span data-ttu-id="d873e-153">**IsDirty**</span><span class="sxs-lookup"><span data-stu-id="d873e-153">**IsDirty**</span></span>](cpersiststream-isdirty.md)                       | <span data-ttu-id="d873e-154">檢查是否必須儲存物件。</span><span class="sxs-lookup"><span data-stu-id="d873e-154">Checks if the object must be saved.</span></span>                                           |
| [<span data-ttu-id="d873e-155">**載入**</span><span class="sxs-lookup"><span data-stu-id="d873e-155">**Load**</span></span>](cpersiststream-load.md)                             | <span data-ttu-id="d873e-156">將資料流程中的資料載入記憶體。</span><span class="sxs-lookup"><span data-stu-id="d873e-156">Loads the data from the stream into memory.</span></span>                                   |
| [<span data-ttu-id="d873e-157">**儲存**</span><span class="sxs-lookup"><span data-stu-id="d873e-157">**Save**</span></span>](cpersiststream-save.md)                             | <span data-ttu-id="d873e-158">將記憶體中的資料儲存至資料流程。</span><span class="sxs-lookup"><span data-stu-id="d873e-158">Saves the data from memory to the stream.</span></span>                                     |



 

 

 
