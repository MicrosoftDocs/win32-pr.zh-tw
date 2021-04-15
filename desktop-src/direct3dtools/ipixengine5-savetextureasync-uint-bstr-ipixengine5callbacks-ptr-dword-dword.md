---
description: 儲存材質。
MS-HAID: vspixengine.IPixEngine5\_SaveTextureAsync\_UINT\_BSTR\_IPixEngine5Callbacks\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixEngine5：： SaveTextureAsync 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 6F08F49E-6FFD-4A9B-86F5-8CB499947F57
api_name:
- IPixEngine5.SaveTextureAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2590f793d0ba05af1ccf9e10ba04fa8b6aa2421b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467920"
---
# <a name="span-idvspixengineipixengine5_savetextureasync_uint_bstr_ipixengine5callbacks_ptr_dword_dwordspanipixengine5savetextureasync-method"></a><span data-ttu-id="ebd0c-103"><span id="vspixengine.ipixengine5_savetextureasync_uint_bstr_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5：： SaveTextureAsync 方法</span><span class="sxs-lookup"><span data-stu-id="ebd0c-103"><span id="vspixengine.ipixengine5_savetextureasync_uint_bstr_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5::SaveTextureAsync method</span></span>

<span data-ttu-id="ebd0c-104">儲存材質。</span><span class="sxs-lookup"><span data-stu-id="ebd0c-104">Saves a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebd0c-105">語法</span><span class="sxs-lookup"><span data-stu-id="ebd0c-105">Syntax</span></span>


```C++
HRESULT SaveTextureAsync(
   UINT                  textureId,
   BSTR                  fileName,
   IPixEngine5Callbacks* callbacks,
   DWORD                 requestCookie,
   DWORD                 progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="ebd0c-106">參數</span><span class="sxs-lookup"><span data-stu-id="ebd0c-106">Parameters</span></span>

<span data-ttu-id="ebd0c-107">*textureId* </span><span class="sxs-lookup"><span data-stu-id="ebd0c-107">*textureId* </span></span>  
<span data-ttu-id="ebd0c-108">要儲存之材質的識別碼。</span><span class="sxs-lookup"><span data-stu-id="ebd0c-108">The ID of the texture to save.</span></span>

<span data-ttu-id="ebd0c-109">*檔案名* </span><span class="sxs-lookup"><span data-stu-id="ebd0c-109">*fileName* </span></span>  
<span data-ttu-id="ebd0c-110">COM 字串，其中包含已儲存材質的路徑名稱。</span><span class="sxs-lookup"><span data-stu-id="ebd0c-110">A COM string containing the pathname of the saved texture.</span></span>

<span data-ttu-id="ebd0c-111">*回檔* </span><span class="sxs-lookup"><span data-stu-id="ebd0c-111">*callbacks* </span></span>  
<span data-ttu-id="ebd0c-112">提供 IPixEngine5 回呼介面之物件的位址。</span><span class="sxs-lookup"><span data-stu-id="ebd0c-112">The address of an object that provides the IPixEngine5 callbacks interface.</span></span>

<span data-ttu-id="ebd0c-113">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="ebd0c-113">*requestCookie* </span></span>  
<span data-ttu-id="ebd0c-114">可唯一識別要求的 cookie，而且可用來指示它被取消。</span><span class="sxs-lookup"><span data-stu-id="ebd0c-114">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="ebd0c-115">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="ebd0c-115">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="ebd0c-116">未使用。</span><span class="sxs-lookup"><span data-stu-id="ebd0c-116">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="ebd0c-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="ebd0c-117">Return value</span></span>

<span data-ttu-id="ebd0c-118">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="ebd0c-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ebd0c-119">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="ebd0c-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebd0c-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="ebd0c-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="ebd0c-121">標頭</span><span class="sxs-lookup"><span data-stu-id="ebd0c-121">Header</span></span></p></td><td><span data-ttu-id="ebd0c-122">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="ebd0c-122">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="ebd0c-123"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="ebd0c-123"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="ebd0c-124">**IPixEngine5**</span><span class="sxs-lookup"><span data-stu-id="ebd0c-124">**IPixEngine5**</span></span>](/windows/desktop/direct3dtools/ipixengine5)

 

 
