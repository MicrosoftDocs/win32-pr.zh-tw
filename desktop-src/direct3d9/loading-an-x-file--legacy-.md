---
description: 在繼承應用程式中使用下列程式載入 x.x 檔案。
ms.assetid: 2b975873-2e5d-4c64-a022-d2098c3d95b8
title: '載入 X 檔案 (舊版)  (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 716ed54afdc7d1aa18fdde992a0799a8990a49c6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104509953"
---
# <a name="loading-an-x-file-legacy-direct3d-9"></a><span data-ttu-id="97b25-103">載入 X 檔案 (舊版)  (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="97b25-103">Loading an X File (Legacy) (Direct3D 9)</span></span>

<span data-ttu-id="97b25-104">在繼承應用程式中使用下列程式載入 x.x 檔案。</span><span class="sxs-lookup"><span data-stu-id="97b25-104">Use the following procedure in legacy applications to load a .x file.</span></span>

1.  <span data-ttu-id="97b25-105">您可以使用 [**DirectXFileCreate**](directxfilecreate.md) 函數來建立 [**IDirectXFile**](idirectxfile.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="97b25-105">Use the [**DirectXFileCreate**](directxfilecreate.md) function to create an [**IDirectXFile**](idirectxfile.md) object.</span></span>
2.  <span data-ttu-id="97b25-106">如果範本存在於您將載入的 DirectX 檔案中，請使用 [**IDirectXFile：： RegisterTemplates**](idirectxfile--registertemplates.md) 方法來註冊這些範本。</span><span class="sxs-lookup"><span data-stu-id="97b25-106">If templates are present in the DirectX file that you will load, use the [**IDirectXFile::RegisterTemplates**](idirectxfile--registertemplates.md) method to register those templates.</span></span>
3.  <span data-ttu-id="97b25-107">使用 [**IDirectXFile：： CreateEnumObject**](idirectxfile--createenumobject.md) 方法來建立 [**IDirectXFileEnumObject**](idirectxfileenumobject.md) 列舉值物件。</span><span class="sxs-lookup"><span data-stu-id="97b25-107">Use the [**IDirectXFile::CreateEnumObject**](idirectxfile--createenumobject.md) method to create an [**IDirectXFileEnumObject**](idirectxfileenumobject.md) enumerator object.</span></span>
4.  <span data-ttu-id="97b25-108">迴圈流覽檔案中的物件。</span><span class="sxs-lookup"><span data-stu-id="97b25-108">Loop through the objects in the file.</span></span> <span data-ttu-id="97b25-109">針對每個物件，執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="97b25-109">For each object, perform the following steps.</span></span>
    1.  <span data-ttu-id="97b25-110">使用 [**IDirectXFileEnumObject：： GetNextDataObject**](idirectxfileenumobject--getnextdataobject.md) 方法來取出每個 [**IDirectXFileData**](idirectxfiledata.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="97b25-110">Use the [**IDirectXFileEnumObject::GetNextDataObject**](idirectxfileenumobject--getnextdataobject.md) method to retrieve each [**IDirectXFileData**](idirectxfiledata.md) object.</span></span>
    2.  <span data-ttu-id="97b25-111">您可以使用 [**IDirectXFileData：： GetType**](idirectxfiledata--gettype.md) 方法來取出資料的型別。</span><span class="sxs-lookup"><span data-stu-id="97b25-111">Use the [**IDirectXFileData::GetType**](idirectxfiledata--gettype.md) method to retrieve the data's type.</span></span>
    3.  <span data-ttu-id="97b25-112">使用 [**IDirectXFileData：：：：**](idirectxfiledata--getdata.md) 的方法載入資料。</span><span class="sxs-lookup"><span data-stu-id="97b25-112">Load the data using the [**IDirectXFileData::GetData**](idirectxfiledata--getdata.md) method.</span></span>
    4.  <span data-ttu-id="97b25-113">如果物件具有選擇性成員，請藉由呼叫 [**IDirectXFileData：： GetNextObject**](idirectxfiledata--getnextobject.md) 方法來取出選擇性成員。</span><span class="sxs-lookup"><span data-stu-id="97b25-113">If the object has optional members, retrieve the optional members by calling the [**IDirectXFileData::GetNextObject**](idirectxfiledata--getnextobject.md) method.</span></span>
    5.  <span data-ttu-id="97b25-114">釋放 [**IDirectXFileData**](idirectxfiledata.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="97b25-114">Release the [**IDirectXFileData**](idirectxfiledata.md) object.</span></span>
5.  <span data-ttu-id="97b25-115">釋放 [**IDirectXFileEnumObject**](idirectxfileenumobject.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="97b25-115">Release the [**IDirectXFileEnumObject**](idirectxfileenumobject.md) object.</span></span>
6.  <span data-ttu-id="97b25-116">釋放 [**IDirectXFile**](idirectxfile.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="97b25-116">Release the [**IDirectXFile**](idirectxfile.md) object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="97b25-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="97b25-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97b25-118">X 檔案 (舊版) </span><span class="sxs-lookup"><span data-stu-id="97b25-118">X Files (Legacy)</span></span>](x-files--legacy-.md)
</dt> </dl>

 

 



