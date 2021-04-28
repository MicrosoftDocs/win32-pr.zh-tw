---
description: DEVICEDIALOGDATA2 結構-定義呼叫裝置對話方塊所需的資料。
ms.assetid: 544238de-310f-4fc3-b519-bb4e6b309272
title: 'DEVICEDIALOGDATA2 結構 (Wiadefd .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DEVICEDIALOGDATA2
api_type:
- HeaderDef
api_location:
- Wiadefd.h
ms.openlocfilehash: 82ca6cba81101e577eed882ad45272ab81546fed
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089801"
---
# <a name="devicedialogdata2-structure"></a><span data-ttu-id="ff1ca-103">DEVICEDIALOGDATA2 結構</span><span class="sxs-lookup"><span data-stu-id="ff1ca-103">DEVICEDIALOGDATA2 structure</span></span>

<span data-ttu-id="ff1ca-104">定義呼叫裝置對話方塊所需的資料。</span><span class="sxs-lookup"><span data-stu-id="ff1ca-104">Defines the data needed to call a device dialog.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff1ca-105">語法</span><span class="sxs-lookup"><span data-stu-id="ff1ca-105">Syntax</span></span>


```C++
typedef struct {
  DWORD     cbSize;
  IWiaItem2 *pIWiaItemRoot;
  DWORD     dwFlags;
  HWND      hwndParent;
  BSTR      bstrFolderName;
  BSTR      bstrFilename;
  LONG      lNumFiles;
  BSTR      *pbstrFilePaths;
  IWiaItem2 *ppWiaItem;
} DEVICEDIALOGDATA2;
```



## <a name="members"></a><span data-ttu-id="ff1ca-106">成員</span><span class="sxs-lookup"><span data-stu-id="ff1ca-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ff1ca-107">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="ff1ca-107">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="ff1ca-108">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="ff1ca-108">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="ff1ca-109">指定此結構的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="ff1ca-109">Specifies the size of this structure in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="ff1ca-110">**pIWiaItemRoot**</span><span class="sxs-lookup"><span data-stu-id="ff1ca-110">**pIWiaItemRoot**</span></span>
</dt> <dd>

<span data-ttu-id="ff1ca-111">類型： **[ **IWiaItem2**](-wia-iwiaitem2.md)\***</span><span class="sxs-lookup"><span data-stu-id="ff1ca-111">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\***</span></span>

</dd> <dd>

<span data-ttu-id="ff1ca-112">指向 [**IWiaItem2**](-wia-iwiaitem2.md) 介面，表示應用程式專案樹狀結構中的有效根專案。</span><span class="sxs-lookup"><span data-stu-id="ff1ca-112">Points to an [**IWiaItem2**](-wia-iwiaitem2.md) interface that represents the valid root item in the application item tree.</span></span>

</dd> <dt>

<span data-ttu-id="ff1ca-113">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="ff1ca-113">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="ff1ca-114">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="ff1ca-114">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="ff1ca-115">指定一組旗標來控制對話方塊的操作。</span><span class="sxs-lookup"><span data-stu-id="ff1ca-115">Specifies a set of flags that control the dialog box's operation.</span></span> <span data-ttu-id="ff1ca-116">可以設定為下列任何值：</span><span class="sxs-lookup"><span data-stu-id="ff1ca-116">Can be set to any of the following values:</span></span>



| <span data-ttu-id="ff1ca-117">旗標</span><span class="sxs-lookup"><span data-stu-id="ff1ca-117">Flag</span></span>                                 | <span data-ttu-id="ff1ca-118">意義</span><span class="sxs-lookup"><span data-stu-id="ff1ca-118">Meaning</span></span>                                                                                                                                                                                     |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff1ca-119">0</span><span class="sxs-lookup"><span data-stu-id="ff1ca-119">0</span></span>                                    | <span data-ttu-id="ff1ca-120">預設行為。</span><span class="sxs-lookup"><span data-stu-id="ff1ca-120">Default behavior.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="ff1ca-121">WIA \_ 裝置 \_ 對話方塊 \_ 單一 \_ 影像</span><span class="sxs-lookup"><span data-stu-id="ff1ca-121">WIA\_DEVICE\_DIALOG\_SINGLE\_IMAGE</span></span>   | <span data-ttu-id="ff1ca-122">在 [裝置映射取得] 對話方塊中，將影像選取範圍限制為單一影像。</span><span class="sxs-lookup"><span data-stu-id="ff1ca-122">Restrict image selection to a single image in the device image acquisition dialog box.</span></span>                                                                                                      |
| <span data-ttu-id="ff1ca-123">WIA \_ 裝置 \_ 對話方塊 \_ 使用 \_ 一般 \_ UI</span><span class="sxs-lookup"><span data-stu-id="ff1ca-123">WIA\_DEVICE\_DIALOG\_USE\_COMMON\_UI</span></span> | <span data-ttu-id="ff1ca-124">使用系統 UI （如果有的話），而不是廠商提供的 UI。</span><span class="sxs-lookup"><span data-stu-id="ff1ca-124">Use the system UI, if available, rather than the vendor-supplied UI.</span></span> <span data-ttu-id="ff1ca-125">如果系統 UI 無法使用，則會使用廠商 UI。</span><span class="sxs-lookup"><span data-stu-id="ff1ca-125">If the system UI is not available, the vendor UI is used.</span></span> <span data-ttu-id="ff1ca-126">如果沒有可用的 UI，函數會傳回 E \_ >notimpl。</span><span class="sxs-lookup"><span data-stu-id="ff1ca-126">If neither UI is available, the function returns E\_NOTIMPL.</span></span> |



 

</dd> <dt>

<span data-ttu-id="ff1ca-127">**hwndParent**</span><span class="sxs-lookup"><span data-stu-id="ff1ca-127">**hwndParent**</span></span>
</dt> <dd>

<span data-ttu-id="ff1ca-128">類型： **HWND**</span><span class="sxs-lookup"><span data-stu-id="ff1ca-128">Type: **HWND**</span></span>

</dd> <dd>

<span data-ttu-id="ff1ca-129">指定對話方塊父視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="ff1ca-129">Specifies the handle to the parent window of the dialog.</span></span>

</dd> <dt>

<span data-ttu-id="ff1ca-130">**bstrFolderName**</span><span class="sxs-lookup"><span data-stu-id="ff1ca-130">**bstrFolderName**</span></span>
</dt> <dd>

<span data-ttu-id="ff1ca-131">類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ff1ca-131">Type: **BSTR**</span></span>

</dd> <dd>

<span data-ttu-id="ff1ca-132">指定要傳送檔案的資料夾名稱。</span><span class="sxs-lookup"><span data-stu-id="ff1ca-132">Specifies the folder name where the files are transferred.</span></span>

</dd> <dt>

<span data-ttu-id="ff1ca-133">**bstrFilename**</span><span class="sxs-lookup"><span data-stu-id="ff1ca-133">**bstrFilename**</span></span>
</dt> <dd>

<span data-ttu-id="ff1ca-134">類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ff1ca-134">Type: **BSTR**</span></span>

</dd> <dd>

<span data-ttu-id="ff1ca-135">指定要用於從 WIA 專案傳輸至 **bstrFolderName** 所指定目的資料夾之檔案的檔案名範本。</span><span class="sxs-lookup"><span data-stu-id="ff1ca-135">Specifies the filename template to be used for files transferred from WIA items to the destination folder designated by **bstrFolderName**.</span></span> <span data-ttu-id="ff1ca-136">您可以將額外的字元附加至檔案名範本，以建立任意數目的唯一檔案名。</span><span class="sxs-lookup"><span data-stu-id="ff1ca-136">An arbitrary number of unique file names can be created by appending additional characters to the file name template.</span></span>

</dd> <dt>

<span data-ttu-id="ff1ca-137">**lNumFiles**</span><span class="sxs-lookup"><span data-stu-id="ff1ca-137">**lNumFiles**</span></span>
</dt> <dd>

<span data-ttu-id="ff1ca-138">類型： **LONG**</span><span class="sxs-lookup"><span data-stu-id="ff1ca-138">Type: **LONG**</span></span>

</dd> <dd>

<span data-ttu-id="ff1ca-139">接收寫入至 **pbstrFilePaths** 陣列的字串數目。</span><span class="sxs-lookup"><span data-stu-id="ff1ca-139">Receives the number of strings written to the **pbstrFilePaths** array.</span></span>

</dd> <dt>

<span data-ttu-id="ff1ca-140">**pbstrFilePaths**</span><span class="sxs-lookup"><span data-stu-id="ff1ca-140">**pbstrFilePaths**</span></span>
</dt> <dd>

<span data-ttu-id="ff1ca-141">類型： **BSTR \***</span><span class="sxs-lookup"><span data-stu-id="ff1ca-141">Type: **BSTR\***</span></span>

</dd> <dd>

<span data-ttu-id="ff1ca-142">指向 BSTR 指標陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="ff1ca-142">Pointer to an array of BSTR pointers.</span></span> <span data-ttu-id="ff1ca-143">每個陣列元素都會指向一個 BSTR，其中包含已成功傳送至 bstrFolderName 所識別之資料夾的檔案目的地名稱。</span><span class="sxs-lookup"><span data-stu-id="ff1ca-143">Each array element points to a BSTR that contains the destination name of a file that was successfully transferred to the folder identified by bstrFolderName.</span></span> <span data-ttu-id="ff1ca-144">方法必須配置這個成員的儲存體。</span><span class="sxs-lookup"><span data-stu-id="ff1ca-144">The method must allocate the storage for this member.</span></span>

</dd> <dt>

<span data-ttu-id="ff1ca-145">**ppWiaItem**</span><span class="sxs-lookup"><span data-stu-id="ff1ca-145">**ppWiaItem**</span></span>
</dt> <dd>

<span data-ttu-id="ff1ca-146">類型： **[ **IWiaItem2**](-wia-iwiaitem2.md)\***</span><span class="sxs-lookup"><span data-stu-id="ff1ca-146">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\***</span></span>

</dd> <dd>

<span data-ttu-id="ff1ca-147">WIA 專案的 [**IWiaItem2**](-wia-iwiaitem2.md) 介面指標，可將資料傳送至 **pbstrFilePaths** 陣列中所命名的檔案或檔案。</span><span class="sxs-lookup"><span data-stu-id="ff1ca-147">Pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) interface of the WIA item that transfers data to the file or files named in the **pbstrFilePaths** array.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ff1ca-148">規格需求</span><span class="sxs-lookup"><span data-stu-id="ff1ca-148">Requirements</span></span>



| <span data-ttu-id="ff1ca-149">需求</span><span class="sxs-lookup"><span data-stu-id="ff1ca-149">Requirement</span></span> | <span data-ttu-id="ff1ca-150">值</span><span class="sxs-lookup"><span data-stu-id="ff1ca-150">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ff1ca-151">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ff1ca-151">Minimum supported client</span></span><br/> | <span data-ttu-id="ff1ca-152">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ff1ca-152">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="ff1ca-153">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ff1ca-153">Minimum supported server</span></span><br/> | <span data-ttu-id="ff1ca-154">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ff1ca-154">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ff1ca-155">標頭</span><span class="sxs-lookup"><span data-stu-id="ff1ca-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff1ca-156"><dt>Wiadefd。h</dt></span><span class="sxs-lookup"><span data-stu-id="ff1ca-156"><dt>Wiadefd.h</dt></span></span> </dl> |



 

 




