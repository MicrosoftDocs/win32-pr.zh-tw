---
description: 開啟圖形記錄檔。
MS-HAID: vspixengine.IPixEngine\_OpenFile\_BSTR\_BSTR\_INewFramesCallback\_ptr\_IFileIOCallback\_ptr\_LCID
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixEngine：： OpenFile 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8E0E1336-9FC7-4C32-AF3C-F3BDF39A36D9
api_name:
- IPixEngine.OpenFile
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d18b0ff4d6d2301c6d52d2bc855d48a3db124ccb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109060"
---
# <a name="span-idvspixengineipixengine_openfile_bstr_bstr_inewframescallback_ptr_ifileiocallback_ptr_lcidspanipixengineopenfile-method"></a><span data-ttu-id="30a23-103"><span id="vspixengine.ipixengine_openfile_bstr_bstr_inewframescallback_ptr_ifileiocallback_ptr_lcid"></span>IPixEngine：： OpenFile 方法</span><span class="sxs-lookup"><span data-stu-id="30a23-103"><span id="vspixengine.ipixengine_openfile_bstr_bstr_inewframescallback_ptr_ifileiocallback_ptr_lcid"></span>IPixEngine::OpenFile method</span></span>

<span data-ttu-id="30a23-104">開啟圖形記錄檔。</span><span class="sxs-lookup"><span data-stu-id="30a23-104">Opens a graphics log.</span></span>

## <a name="syntax"></a><span data-ttu-id="30a23-105">語法</span><span class="sxs-lookup"><span data-stu-id="30a23-105">Syntax</span></span>


```C++
HRESULT OpenFile(
   BSTR                FileName,
   BSTR                registryBoot,
   INewFramesCallback* callbacks,
   IFileIOCallback*    pFileIOCallback,
   LCID                uiLocale
);
```

## <a name="parameters"></a><span data-ttu-id="30a23-106">參數</span><span class="sxs-lookup"><span data-stu-id="30a23-106">Parameters</span></span>

<span data-ttu-id="30a23-107">*檔案名* </span><span class="sxs-lookup"><span data-stu-id="30a23-107">*FileName* </span></span>  
<span data-ttu-id="30a23-108">COM 字串，包含圖形記錄檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="30a23-108">A COM string containing the name of the graphics log.</span></span>

<span data-ttu-id="30a23-109">*registryBoot* </span><span class="sxs-lookup"><span data-stu-id="30a23-109">*registryBoot* </span></span>  
<span data-ttu-id="30a23-110">包含登錄根目錄的 COM 字串。</span><span class="sxs-lookup"><span data-stu-id="30a23-110">A COM string containing the registry root.</span></span> <span data-ttu-id="30a23-111">引擎會在此尋找 DIA 和其他登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="30a23-111">The engine looks here for DIA and other registry keys.</span></span>

<span data-ttu-id="30a23-112">*回檔* </span><span class="sxs-lookup"><span data-stu-id="30a23-112">*callbacks* </span></span>  
<span data-ttu-id="30a23-113">用來通知主機已剖析新框架的函式位址。</span><span class="sxs-lookup"><span data-stu-id="30a23-113">The address of a function used to notify the host that new frames have been parsed.</span></span>

<span data-ttu-id="30a23-114">*pFileIOCallback* </span><span class="sxs-lookup"><span data-stu-id="30a23-114">*pFileIOCallback* </span></span>  
<span data-ttu-id="30a23-115">用來在剖析期間通知主機檔案 IO 錯誤的函式位址。</span><span class="sxs-lookup"><span data-stu-id="30a23-115">The address of a function used to notify the host of file IO errors during parsing.</span></span>

<span data-ttu-id="30a23-116">*uiLocale* </span><span class="sxs-lookup"><span data-stu-id="30a23-116">*uiLocale* </span></span>  
<span data-ttu-id="30a23-117">用來根據地區設定顯示錯誤訊息的地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="30a23-117">The locale ID used to present error messages according to locale settings.</span></span>

## <a name="return-value"></a><span data-ttu-id="30a23-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="30a23-118">Return value</span></span>

<span data-ttu-id="30a23-119">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="30a23-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="30a23-120">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="30a23-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="30a23-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="30a23-121">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="30a23-122">標頭</span><span class="sxs-lookup"><span data-stu-id="30a23-122">Header</span></span></p></td><td><span data-ttu-id="30a23-123">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="30a23-123">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="30a23-124"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="30a23-124"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="30a23-125">**IPixEngine**</span><span class="sxs-lookup"><span data-stu-id="30a23-125">**IPixEngine**</span></span>](/windows/desktop/direct3dtools/ipixengine)

 

 
