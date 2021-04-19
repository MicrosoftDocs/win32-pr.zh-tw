---
description: 建立儲存物件，該物件將用來將資料儲存至 x.x 檔案。
ms.assetid: da064e83-605f-4c86-985d-9a0961c18e01
title: 'ID3DXFile：： CreateSaveObject 方法 (D3DX9Xof .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFile.CreateSaveObject
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d7c5b3de020ad50abfd8834aabbdc8e6e848d71d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106985534"
---
# <a name="id3dxfilecreatesaveobject-method"></a><span data-ttu-id="c5965-103">ID3DXFile：： CreateSaveObject 方法</span><span class="sxs-lookup"><span data-stu-id="c5965-103">ID3DXFile::CreateSaveObject method</span></span>

<span data-ttu-id="c5965-104">建立儲存物件，該物件將用來將資料儲存至 x.x 檔案。</span><span class="sxs-lookup"><span data-stu-id="c5965-104">Creates a save object that will be used to save data to a .x file.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5965-105">語法</span><span class="sxs-lookup"><span data-stu-id="c5965-105">Syntax</span></span>


```C++
HRESULT CreateSaveObject(
  [in]  LPCVOID               pData,
  [in]  D3DXF_FILESAVEOPTIONS flags,
  [in]  D3DXF_FILEFORMAT      dwFileFormat,
  [out] ID3DXFileSaveObject   **ppSaveObj
);
```



## <a name="parameters"></a><span data-ttu-id="c5965-106">參數</span><span class="sxs-lookup"><span data-stu-id="c5965-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5965-107">*.pdata* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c5965-107">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5965-108">類型： **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c5965-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c5965-109">要用來儲存資料的檔案名指標。</span><span class="sxs-lookup"><span data-stu-id="c5965-109">Pointer to the name of the file to use for saving data.</span></span>

</dd> <dt>

<span data-ttu-id="c5965-110">*旗標* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c5965-110">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5965-111">類型： **[D3DXF \_ FILESAVEOPTIONS](d3dxf.md)**</span><span class="sxs-lookup"><span data-stu-id="c5965-111">Type: **[D3DXF\_FILESAVEOPTIONS](d3dxf.md)**</span></span>

<span data-ttu-id="c5965-112">值，指定要儲存資料的檔案名。</span><span class="sxs-lookup"><span data-stu-id="c5965-112">Value that specifies the name of the file to which data is to be saved.</span></span> <span data-ttu-id="c5965-113">這個值可以是其中一個 [ [儲存選項](d3dxf.md) ] 旗標。</span><span class="sxs-lookup"><span data-stu-id="c5965-113">This value can be one of the [File Save Options](d3dxf.md) flags.</span></span>

</dd> <dt>

<span data-ttu-id="c5965-114">*dwFileFormat* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c5965-114">*dwFileFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5965-115">類型： **[D3DXF \_ >fileformat](d3dxf.md)**</span><span class="sxs-lookup"><span data-stu-id="c5965-115">Type: **[D3DXF\_FILEFORMAT](d3dxf.md)**</span></span>

<span data-ttu-id="c5965-116">指出儲存. x 檔案時要使用的格式。</span><span class="sxs-lookup"><span data-stu-id="c5965-116">Indicates the format to use when saving the .x file.</span></span> <span data-ttu-id="c5965-117">這個值可以是其中一個 [檔案格式](d3dxf.md) 旗標。</span><span class="sxs-lookup"><span data-stu-id="c5965-117">This value can be one of the [File Formats](d3dxf.md) flags.</span></span> <span data-ttu-id="c5965-118">如需詳細資訊，請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="c5965-118">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="c5965-119">*ppSaveObj* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c5965-119">*ppSaveObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c5965-120">類型： **[ **ID3DXFileSaveObject**](id3dxfilesaveobject.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="c5965-120">Type: **[**ID3DXFileSaveObject**](id3dxfilesaveobject.md)\*\***</span></span>

<span data-ttu-id="c5965-121">[**ID3DXFileSaveObject**](id3dxfilesaveobject.md)介面指標的位址，表示所建立的儲存物件。</span><span class="sxs-lookup"><span data-stu-id="c5965-121">Address of a pointer to an [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) interface, representing the created save object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5965-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="c5965-122">Return value</span></span>

<span data-ttu-id="c5965-123">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c5965-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c5965-124">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="c5965-124">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="c5965-125">如果方法失敗，則傳回值可以是下列其中一項： D3DXFERR \_ BADVALUE，D3DXFERR \_ PARSEERROR。</span><span class="sxs-lookup"><span data-stu-id="c5965-125">If the method fails, the return value can be one of the following: D3DXFERR\_BADVALUE, D3DXFERR\_PARSEERROR.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5965-126">備註</span><span class="sxs-lookup"><span data-stu-id="c5965-126">Remarks</span></span>

<span data-ttu-id="c5965-127">使用這個方法之後，請使用 [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) 介面的方法來建立資料物件，以及儲存範本或資料。</span><span class="sxs-lookup"><span data-stu-id="c5965-127">After using this method, use methods of the [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) interface to create data objects and to save templates or data.</span></span>

<span data-ttu-id="c5965-128">針對已儲存的檔案格式 *dwFileFormat*，必須指定 [檔案格式](d3dxf.md) 中的其中一個二進位檔、舊版二進位檔或文字旗標。</span><span class="sxs-lookup"><span data-stu-id="c5965-128">For the saved file format *dwFileFormat*, one of the binary, legacy binary, or text flags in [File Formats](d3dxf.md) must be specified.</span></span> <span data-ttu-id="c5965-129">您可以使用選擇性的 D3DXF \_ >fileformat 壓縮旗標來壓縮檔案 \_ 。</span><span class="sxs-lookup"><span data-stu-id="c5965-129">The file can be compressed by using the optional D3DXF\_FILEFORMAT\_COMPRESSED flag.</span></span>

<span data-ttu-id="c5965-130">您可以將檔案格式值結合成邏輯 OR，以建立壓縮的文字或壓縮的二進位檔案。</span><span class="sxs-lookup"><span data-stu-id="c5965-130">The file format values can be combined in a logical OR to create compressed text or compressed binary files.</span></span> <span data-ttu-id="c5965-131">如果您指出檔案格式應該是文字並壓縮檔案，則會先將檔案寫出為文字，然後壓縮。</span><span class="sxs-lookup"><span data-stu-id="c5965-131">If you indicate that the file format should be text and compressed, the file will be written out first as text and then compressed.</span></span> <span data-ttu-id="c5965-132">不過，壓縮的文字檔不如二進位文字檔一樣有效率;因此，在大部分情況下，您會想要指出二進位和壓縮。</span><span class="sxs-lookup"><span data-stu-id="c5965-132">However, compressed text files are not as efficient as binary text files; in most cases, therefore, you will want to indicate binary and compressed.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5965-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="c5965-133">Requirements</span></span>



| <span data-ttu-id="c5965-134">需求</span><span class="sxs-lookup"><span data-stu-id="c5965-134">Requirement</span></span> | <span data-ttu-id="c5965-135">值</span><span class="sxs-lookup"><span data-stu-id="c5965-135">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c5965-136">標頭</span><span class="sxs-lookup"><span data-stu-id="c5965-136">Header</span></span><br/>  | <dl> <span data-ttu-id="c5965-137"><dt>D3DX9Xof。h</dt></span><span class="sxs-lookup"><span data-stu-id="c5965-137"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="c5965-138">程式庫</span><span class="sxs-lookup"><span data-stu-id="c5965-138">Library</span></span><br/> | <dl> <span data-ttu-id="c5965-139"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c5965-139"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="c5965-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c5965-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5965-141">ID3DXFile</span><span class="sxs-lookup"><span data-stu-id="c5965-141">ID3DXFile</span></span>](id3dxfile.md)
</dt> <dt>

[<span data-ttu-id="c5965-142">**ID3DXFileSaveObject**</span><span class="sxs-lookup"><span data-stu-id="c5965-142">**ID3DXFileSaveObject**</span></span>](id3dxfilesaveobject.md)
</dt> </dl>

 

 
