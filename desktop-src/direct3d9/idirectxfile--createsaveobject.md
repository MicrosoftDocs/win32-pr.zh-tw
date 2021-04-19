---
description: 建立儲存物件。 已取代。
ms.assetid: 50a7dbde-1dd4-4aae-a9ab-97d6f99618c0
title: 'IDirectXFile：： CreateSaveObject 方法 (DXFile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFile.CreateSaveObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 848010a1f701b39f5cc77a126272bc019ed01f4f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106988209"
---
# <a name="idirectxfilecreatesaveobject-method"></a><span data-ttu-id="2e923-104">IDirectXFile：： CreateSaveObject 方法</span><span class="sxs-lookup"><span data-stu-id="2e923-104">IDirectXFile::CreateSaveObject method</span></span>

<span data-ttu-id="2e923-105">建立儲存物件。</span><span class="sxs-lookup"><span data-stu-id="2e923-105">Creates a save object.</span></span> <span data-ttu-id="2e923-106">已取代。</span><span class="sxs-lookup"><span data-stu-id="2e923-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e923-107">語法</span><span class="sxs-lookup"><span data-stu-id="2e923-107">Syntax</span></span>


```C++
HRESULT CreateSaveObject(
  [in]          LPCSTR                  szFileName,
  [in]          DXFILEFORMAT            dwFileFormat,
  [out, retval] LPDIRECTXFILESAVEOBJECT *ppSaveObj
);
```



## <a name="parameters"></a><span data-ttu-id="2e923-108">參數</span><span class="sxs-lookup"><span data-stu-id="2e923-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e923-109">*szFileName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2e923-109">*szFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e923-110">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2e923-110">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2e923-111">要用來儲存資料的檔案名指標。</span><span class="sxs-lookup"><span data-stu-id="2e923-111">Pointer to the name of the file to use for saving data.</span></span>

</dd> <dt>

<span data-ttu-id="2e923-112">*dwFileFormat* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2e923-112">*dwFileFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e923-113">類型： **[ **DXFILEFORMAT**](dxfile.md)**</span><span class="sxs-lookup"><span data-stu-id="2e923-113">Type: **[**DXFILEFORMAT**](dxfile.md)**</span></span>

<span data-ttu-id="2e923-114">指出儲存 DirectX 檔案時要使用的格式。</span><span class="sxs-lookup"><span data-stu-id="2e923-114">Indicates the format to use when saving the DirectX file.</span></span> <span data-ttu-id="2e923-115">這個值可以是 \_ [DXFILE 常數](dxfile.md)中的其中一個 DXFILEFORMAT xxx 旗標。</span><span class="sxs-lookup"><span data-stu-id="2e923-115">This value can be one of the DXFILEFORMAT\_xxx flags in [DXFILE Constants](dxfile.md).</span></span> <span data-ttu-id="2e923-116">如需詳細資訊，請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="2e923-116">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="2e923-117">*ppSaveObj* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="2e923-117">*ppSaveObj* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="2e923-118">類型： **[ **LPDIRECTXFILESAVEOBJECT**](idirectxfilesaveobject.md)\***</span><span class="sxs-lookup"><span data-stu-id="2e923-118">Type: **[**LPDIRECTXFILESAVEOBJECT**](idirectxfilesaveobject.md)\***</span></span>

<span data-ttu-id="2e923-119">[**IDirectXFileSaveObject**](idirectxfilesaveobject.md)介面指標的位址，表示所建立的儲存物件。</span><span class="sxs-lookup"><span data-stu-id="2e923-119">Address of a pointer to an [**IDirectXFileSaveObject**](idirectxfilesaveobject.md) interface, representing the created save object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e923-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="2e923-120">Return value</span></span>

<span data-ttu-id="2e923-121">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2e923-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2e923-122">如果方法成功，則傳回值為 DXFILE \_ OK。</span><span class="sxs-lookup"><span data-stu-id="2e923-122">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="2e923-123">如果方法失敗，則傳回值可以是下列其中一項： DXFILEERR \_ BADALLOC、DXFILEERR \_ BADFILE、DXFILEERR \_ BADVALUE。</span><span class="sxs-lookup"><span data-stu-id="2e923-123">If the method fails, the return value can be one of the following: DXFILEERR\_BADALLOC, DXFILEERR\_BADFILE, DXFILEERR\_BADVALUE.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e923-124">備註</span><span class="sxs-lookup"><span data-stu-id="2e923-124">Remarks</span></span>

<span data-ttu-id="2e923-125">使用這個方法之後，請使用 [**IDirectXFileSaveObject**](idirectxfilesaveobject.md) 介面的方法來建立資料物件，以及儲存範本或資料。</span><span class="sxs-lookup"><span data-stu-id="2e923-125">After using this method, use methods of the [**IDirectXFileSaveObject**](idirectxfilesaveobject.md) interface to create data objects and to save templates or data.</span></span>

<span data-ttu-id="2e923-126">檔案格式的預設值為 DXFILEFORMAT \_ BINARY。</span><span class="sxs-lookup"><span data-stu-id="2e923-126">The default value for the file format is DXFILEFORMAT\_BINARY.</span></span> <span data-ttu-id="2e923-127">您可以將檔案格式值結合成邏輯 OR，以建立壓縮的文字或壓縮的二進位檔案。</span><span class="sxs-lookup"><span data-stu-id="2e923-127">The file format values can be combined in a logical OR to create compressed text or compressed binary files.</span></span> <span data-ttu-id="2e923-128">如果將檔案指定為二進位 (0) 和文字 (1) ，則會將它儲存為文字檔，因為該值將與文本檔案格式值（ (0 + 1 = 1) ）不區分。</span><span class="sxs-lookup"><span data-stu-id="2e923-128">If a file is specified as both binary (0) and text (1), it will be saved as a text file because the value will be indistinguishable from the text file format value (0 + 1 = 1).</span></span> <span data-ttu-id="2e923-129">如果您指出檔案格式應為文字和壓縮檔案格式，則會先將檔案寫出為文字，然後壓縮。</span><span class="sxs-lookup"><span data-stu-id="2e923-129">If you indicate that the file format should be text and compressed, the file will first be written out as text and then compressed.</span></span> <span data-ttu-id="2e923-130">不過，壓縮文字檔的效率不如二進位文字檔，因此在大部分情況下，您會想要指出二進位檔和壓縮檔案。</span><span class="sxs-lookup"><span data-stu-id="2e923-130">However, compressed text files are not as efficient as binary text files, so in most cases you will want to indicate binary and compressed.</span></span> <span data-ttu-id="2e923-131">設定要壓縮但未指定格式的檔案，將會產生二進位、壓縮檔案。</span><span class="sxs-lookup"><span data-stu-id="2e923-131">Setting a file to be compressed without specifying a format will result in a binary, compressed file.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e923-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="2e923-132">Requirements</span></span>



| <span data-ttu-id="2e923-133">需求</span><span class="sxs-lookup"><span data-stu-id="2e923-133">Requirement</span></span> | <span data-ttu-id="2e923-134">值</span><span class="sxs-lookup"><span data-stu-id="2e923-134">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2e923-135">標頭</span><span class="sxs-lookup"><span data-stu-id="2e923-135">Header</span></span><br/>  | <dl> <span data-ttu-id="2e923-136"><dt>DXFile。h</dt></span><span class="sxs-lookup"><span data-stu-id="2e923-136"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="2e923-137">程式庫</span><span class="sxs-lookup"><span data-stu-id="2e923-137">Library</span></span><br/> | <dl> <span data-ttu-id="2e923-138"><dt>D3dxof .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2e923-138"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e923-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2e923-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e923-140">IDirectXFile</span><span class="sxs-lookup"><span data-stu-id="2e923-140">IDirectXFile</span></span>](idirectxfile.md)
</dt> <dt>

[<span data-ttu-id="2e923-141">**IDirectXFileSaveObject**</span><span class="sxs-lookup"><span data-stu-id="2e923-141">**IDirectXFileSaveObject**</span></span>](idirectxfilesaveobject.md)
</dt> </dl>

 

 
