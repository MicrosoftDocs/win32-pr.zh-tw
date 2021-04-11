---
description: 在繼承應用程式中使用下列程式，將. x 檔案範本和資料儲存至 x.x 檔案。
ms.assetid: 5401b381-3599-465a-b41b-e63b7372fc0e
title: '儲存至 X 檔案 (舊版)  (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 467f824c8e3ab9cd360a93d3f69fd1a2352548ae
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104317655"
---
# <a name="saving-to-an-x-file-legacy-direct3d-9"></a><span data-ttu-id="e0737-103">儲存至 X 檔案 (舊版)  (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="e0737-103">Saving to an X File (Legacy) (Direct3D 9)</span></span>

<span data-ttu-id="e0737-104">在繼承應用程式中使用下列程式，將. x 檔案範本和資料儲存至 x.x 檔案。</span><span class="sxs-lookup"><span data-stu-id="e0737-104">Use the following procedure in legacy applications to save .x file templates and data to a .x file.</span></span>

1.  <span data-ttu-id="e0737-105">您可以使用 [**DirectXFileCreate**](directxfilecreate.md) 函數來建立 [**IDirectXFile**](idirectxfile.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="e0737-105">Use the [**DirectXFileCreate**](directxfilecreate.md) function to create an [**IDirectXFile**](idirectxfile.md) object.</span></span>
2.  <span data-ttu-id="e0737-106">使用 [**IDirectXFile：： RegisterTemplates**](idirectxfile--registertemplates.md) 方法，通知 DirectX 檔案系統有關您將使用的任何範本。</span><span class="sxs-lookup"><span data-stu-id="e0737-106">Use the [**IDirectXFile::RegisterTemplates**](idirectxfile--registertemplates.md) method to inform the DirectX file system about any templates that you will use.</span></span>
3.  <span data-ttu-id="e0737-107">使用 [**IDirectXFile：： CreateSaveObject**](idirectxfile--createsaveobject.md) 方法來建立 [**IDirectXFileSaveObject**](idirectxfilesaveobject.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="e0737-107">Use the [**IDirectXFile::CreateSaveObject**](idirectxfile--createsaveobject.md) method to create an [**IDirectXFileSaveObject**](idirectxfilesaveobject.md) object.</span></span>
4.  <span data-ttu-id="e0737-108">如有需要，請使用 [**IDirectXFileSaveObject：： SaveTemplates**](idirectxfilesaveobject--savetemplates.md) 方法來儲存範本。</span><span class="sxs-lookup"><span data-stu-id="e0737-108">Use the [**IDirectXFileSaveObject::SaveTemplates**](idirectxfilesaveobject--savetemplates.md) method to save templates, if desired.</span></span>
5.  <span data-ttu-id="e0737-109">迴圈處理要儲存的物件。</span><span class="sxs-lookup"><span data-stu-id="e0737-109">Loop through the objects to save.</span></span> <span data-ttu-id="e0737-110">針對每個最上層物件，執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="e0737-110">For each top-level object, perform the following steps.</span></span>
    -   <span data-ttu-id="e0737-111">使用 [**IDirectXFileSaveObject：： CreateDataObject**](idirectxfilesaveobject--createdataobject.md) 方法來建立 [**IDirectXFileData**](idirectxfiledata.md) 物件，做為檔案中的最上層物件。</span><span class="sxs-lookup"><span data-stu-id="e0737-111">Use the [**IDirectXFileSaveObject::CreateDataObject**](idirectxfilesaveobject--createdataobject.md) method to create an [**IDirectXFileData**](idirectxfiledata.md) object as a top-level object in the file.</span></span> <span data-ttu-id="e0737-112">如果最上層資料物件有選擇性的子物件，請使用下一個步驟中的適當方法，將它們新增至物件。</span><span class="sxs-lookup"><span data-stu-id="e0737-112">If the top-level data object has optional child objects, add them to the object by using the appropriate method from the next step.</span></span>
    -   <span data-ttu-id="e0737-113">如果物件的範本允許，每個 [**IDirectXFileData**](idirectxfiledata.md) 物件都可以有選擇性的子物件。</span><span class="sxs-lookup"><span data-stu-id="e0737-113">Each [**IDirectXFileData**](idirectxfiledata.md) object can have optional child objects if its template allows it.</span></span> <span data-ttu-id="e0737-114">子物件可以是下列三種類型的物件之一： **IDirectXFileData**、 [**IDirectXFileDataReference**](idirectxfiledatareference.md)或 [**IDirectXFileBinary**](idirectxfilebinary.md)。</span><span class="sxs-lookup"><span data-stu-id="e0737-114">The child objects can be any of the three types of objects: **IDirectXFileData**, [**IDirectXFileDataReference**](idirectxfiledatareference.md), or [**IDirectXFileBinary**](idirectxfilebinary.md).</span></span> <span data-ttu-id="e0737-115">迴圈處理您需要儲存的物件，將每個選擇性的子成員以適當的類型加入至物件清單，如下列步驟所示。</span><span class="sxs-lookup"><span data-stu-id="e0737-115">Loop through the objects you need to save, adding each optional child member to the object list in the manner appropriate to its type, as illustrated in the following steps.</span></span> <span data-ttu-id="e0737-116">然後，如果物件類型是 Data，請呼叫 [**IDirectXFileSaveObject：： CreateDataObject**](idirectxfilesaveobject--createdataobject.md) 方法來建立 **IDirectXFileData** 物件，然後呼叫 [**IDirectXFileData：： AddDataObject**](idirectxfiledata--adddataobject.md) 方法，將它新增為物件的子系。</span><span class="sxs-lookup"><span data-stu-id="e0737-116">Then, if the object type is Data, call the [**IDirectXFileSaveObject::CreateDataObject**](idirectxfilesaveobject--createdataobject.md) method to create an **IDirectXFileData** object, and then call the [**IDirectXFileData::AddDataObject**](idirectxfiledata--adddataobject.md) method to add it as a child of the object.</span></span> <span data-ttu-id="e0737-117">如果物件類型是資料參考，請呼叫 [**IDirectXFileData：： AddDataReference**](idirectxfiledata--adddatareference.md) 方法，以建立資料參考物件，並將其加入為物件的子系。</span><span class="sxs-lookup"><span data-stu-id="e0737-117">If the object type is Data Reference, call the [**IDirectXFileData::AddDataReference**](idirectxfiledata--adddatareference.md) method to create and add the data reference object as a child of the object.</span></span> <span data-ttu-id="e0737-118">或者，如果物件類型是 Binary，請呼叫 [**IDirectXFileData：： AddBinaryObject**](idirectxfiledata--addbinaryobject.md) 方法，以建立二進位物件，並將其新增為物件的子系。</span><span class="sxs-lookup"><span data-stu-id="e0737-118">Or, if the object type is Binary, call the [**IDirectXFileData::AddBinaryObject**](idirectxfiledata--addbinaryobject.md) method to create and add the binary object as a child of the object.</span></span>
    -   <span data-ttu-id="e0737-119">呼叫 [**IDirectXFileSaveObject：： SaveData**](idirectxfilesaveobject--savedata.md) 方法，以儲存資料物件和其子系。</span><span class="sxs-lookup"><span data-stu-id="e0737-119">Call the [**IDirectXFileSaveObject::SaveData**](idirectxfilesaveobject--savedata.md) method to save the data object and its children.</span></span>
    -   <span data-ttu-id="e0737-120">釋放 [**IDirectXFileData**](idirectxfiledata.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="e0737-120">Release the [**IDirectXFileData**](idirectxfiledata.md) object.</span></span>
6.  <span data-ttu-id="e0737-121">釋放 [**IDirectXFileSaveObject**](idirectxfilesaveobject.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="e0737-121">Release the [**IDirectXFileSaveObject**](idirectxfilesaveobject.md) object.</span></span>
7.  <span data-ttu-id="e0737-122">釋放 [**IDirectXFile**](idirectxfile.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="e0737-122">Release the [**IDirectXFile**](idirectxfile.md) object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e0737-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="e0737-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0737-124">X 檔案 (舊版) </span><span class="sxs-lookup"><span data-stu-id="e0737-124">X Files (Legacy)</span></span>](x-files--legacy-.md)
</dt> </dl>

 

 



