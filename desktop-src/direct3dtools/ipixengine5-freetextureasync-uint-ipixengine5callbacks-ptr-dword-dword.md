---
description: 釋出材質，並以非同步方式通知主機。
MS-HAID: vspixengine.IPixEngine5\_FreeTextureAsync\_UINT\_IPixEngine5Callbacks\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixEngine5：： FreeTextureAsync 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9A2D46D4-AA09-4E50-8109-774CE7F538E7
api_name:
- IPixEngine5.FreeTextureAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: aed7d29653b9da6f39b1ef6ec4e600c1857744f2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467905"
---
# <a name="span-idvspixengineipixengine5_freetextureasync_uint_ipixengine5callbacks_ptr_dword_dwordspanipixengine5freetextureasync-method"></a><span data-ttu-id="4b2ad-103"><span id="vspixengine.ipixengine5_freetextureasync_uint_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5：： FreeTextureAsync 方法</span><span class="sxs-lookup"><span data-stu-id="4b2ad-103"><span id="vspixengine.ipixengine5_freetextureasync_uint_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5::FreeTextureAsync method</span></span>

<span data-ttu-id="4b2ad-104">釋出材質，並以非同步方式通知主機。</span><span class="sxs-lookup"><span data-stu-id="4b2ad-104">Frees a texture and notifies the host asynchronously.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b2ad-105">語法</span><span class="sxs-lookup"><span data-stu-id="4b2ad-105">Syntax</span></span>


```C++
HRESULT FreeTextureAsync(
   UINT                  textureId,
   IPixEngine5Callbacks* callbacks,
   DWORD                 requestCookie,
   DWORD                 progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="4b2ad-106">參數</span><span class="sxs-lookup"><span data-stu-id="4b2ad-106">Parameters</span></span>

<span data-ttu-id="4b2ad-107">*textureId* </span><span class="sxs-lookup"><span data-stu-id="4b2ad-107">*textureId* </span></span>  
<span data-ttu-id="4b2ad-108">要釋放之材質的識別碼。</span><span class="sxs-lookup"><span data-stu-id="4b2ad-108">The ID of the texture to free..</span></span>

<span data-ttu-id="4b2ad-109">*回檔* </span><span class="sxs-lookup"><span data-stu-id="4b2ad-109">*callbacks* </span></span>  
<span data-ttu-id="4b2ad-110">提供 IPixEngine5 回呼介面之物件的位址。</span><span class="sxs-lookup"><span data-stu-id="4b2ad-110">The address of an object that provides the IPixEngine5 callbacks interface.</span></span>

<span data-ttu-id="4b2ad-111">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="4b2ad-111">*requestCookie* </span></span>  
<span data-ttu-id="4b2ad-112">可唯一 idenfies 要求的 cookie，而且可用來指示它被取消。</span><span class="sxs-lookup"><span data-stu-id="4b2ad-112">A cookie that uniquely idenfies the request, and can be used to signal for it to be canceled.</span></span>

<span data-ttu-id="4b2ad-113">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="4b2ad-113">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="4b2ad-114">未使用。</span><span class="sxs-lookup"><span data-stu-id="4b2ad-114">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="4b2ad-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="4b2ad-115">Return value</span></span>

<span data-ttu-id="4b2ad-116">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="4b2ad-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4b2ad-117">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="4b2ad-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b2ad-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="4b2ad-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="4b2ad-119">標頭</span><span class="sxs-lookup"><span data-stu-id="4b2ad-119">Header</span></span></p></td><td><span data-ttu-id="4b2ad-120">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="4b2ad-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="4b2ad-121"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="4b2ad-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="4b2ad-122">**IPixEngine5**</span><span class="sxs-lookup"><span data-stu-id="4b2ad-122">**IPixEngine5**</span></span>](/windows/desktop/direct3dtools/ipixengine5)

 

 
