---
description: 註冊自訂範本。 已取代。
ms.assetid: f9b24800-83a5-45bf-b19f-b247c88a2c2c
title: 'IDirectXFile：： RegisterTemplates 方法 (DXFile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFile.RegisterTemplates
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 683a495398e7fe0718ee0642c7760b0a8590538c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106991455"
---
# <a name="idirectxfileregistertemplates-method"></a><span data-ttu-id="2045c-104">IDirectXFile：： RegisterTemplates 方法</span><span class="sxs-lookup"><span data-stu-id="2045c-104">IDirectXFile::RegisterTemplates method</span></span>

<span data-ttu-id="2045c-105">註冊自訂範本。</span><span class="sxs-lookup"><span data-stu-id="2045c-105">Registers custom templates.</span></span> <span data-ttu-id="2045c-106">已取代。</span><span class="sxs-lookup"><span data-stu-id="2045c-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="2045c-107">語法</span><span class="sxs-lookup"><span data-stu-id="2045c-107">Syntax</span></span>


```C++
HRESULT RegisterTemplates(
  [in] LPVOID pvData,
  [in] DWORD  cbSize
);
```



## <a name="parameters"></a><span data-ttu-id="2045c-108">參數</span><span class="sxs-lookup"><span data-stu-id="2045c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2045c-109">*pvData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2045c-109">*pvData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2045c-110">類型： **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2045c-110">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2045c-111">緩衝區的指標，此緩衝區是由包含範本的文字或二進位格式的 DirectX 檔案所組成。</span><span class="sxs-lookup"><span data-stu-id="2045c-111">Pointer to a buffer consisting of a DirectX file in text or binary format that contains templates.</span></span>

</dd> <dt>

<span data-ttu-id="2045c-112">*cbSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2045c-112">*cbSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2045c-113">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2045c-113">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2045c-114">PvData 所指向的緩衝區大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="2045c-114">Size of the buffer pointed to by pvData, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2045c-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="2045c-115">Return value</span></span>

<span data-ttu-id="2045c-116">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2045c-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2045c-117">如果方法成功，則傳回值為 DXFILE \_ OK。</span><span class="sxs-lookup"><span data-stu-id="2045c-117">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="2045c-118">如果方法失敗，則傳回值可以是下列其中一個值： DXFILEERR \_ BADFILEFLOATSIZE、DXFILEERR \_ BADFILETYPE、DXFILEERR \_ BADFILEVERSION、DXFILEERR \_ BADVALUE、DXFILEERR \_ PARSEERROR。</span><span class="sxs-lookup"><span data-stu-id="2045c-118">If the method fails, the return value can be one of the following values: DXFILEERR\_BADFILEFLOATSIZE, DXFILEERR\_BADFILETYPE, DXFILEERR\_BADFILEVERSION, DXFILEERR\_BADVALUE, DXFILEERR\_PARSEERROR.</span></span>

## <a name="remarks"></a><span data-ttu-id="2045c-119">備註</span><span class="sxs-lookup"><span data-stu-id="2045c-119">Remarks</span></span>

<span data-ttu-id="2045c-120">下列程式碼片段提供 **RegisterTemplates** 的範例呼叫，以及 pvData 所指向之緩衝區的範例內容。</span><span class="sxs-lookup"><span data-stu-id="2045c-120">The following code fragment provides an example call to **RegisterTemplates** And example contents for the buffer to which pvData points.</span></span>


```
    TIDirectXFile * pDXFile;
    char *szTemplates = "xof 0303txt 0032\
        template SimpleData { \
            <2b934580-9e9a-11cf-ab39-0020af71e433> \
            DWORD item1;DWORD item2;DWORD item3;} \
        template ArrayData { \
            <2b934581-9e9a-11cf-ab39-0020af71e433> \
            DWORD cItems; array DWORD aItem[2][cItems]; [...] } \
        template RestrictedData { \
            <2b934582-9e9a-11cf-ab39-0020af71e433> \
            DWORD item; [SimpleData]}";
    hr = pDXFile->RegisterTemplates(szTemplates, strlen(szTemplates));
    
    
```



<span data-ttu-id="2045c-121">所有範本都必須指定名稱，以及 (UUID) 的通用唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="2045c-121">All templates must specify a name and a Universally Unique Identifier (UUID).</span></span>

## <a name="requirements"></a><span data-ttu-id="2045c-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="2045c-122">Requirements</span></span>



| <span data-ttu-id="2045c-123">需求</span><span class="sxs-lookup"><span data-stu-id="2045c-123">Requirement</span></span> | <span data-ttu-id="2045c-124">值</span><span class="sxs-lookup"><span data-stu-id="2045c-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2045c-125">標頭</span><span class="sxs-lookup"><span data-stu-id="2045c-125">Header</span></span><br/>  | <dl> <span data-ttu-id="2045c-126"><dt>DXFile。h</dt></span><span class="sxs-lookup"><span data-stu-id="2045c-126"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="2045c-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="2045c-127">Library</span></span><br/> | <dl> <span data-ttu-id="2045c-128"><dt>D3dxof .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2045c-128"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2045c-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2045c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2045c-130">IDirectXFile</span><span class="sxs-lookup"><span data-stu-id="2045c-130">IDirectXFile</span></span>](idirectxfile.md)
</dt> </dl>

 

 
