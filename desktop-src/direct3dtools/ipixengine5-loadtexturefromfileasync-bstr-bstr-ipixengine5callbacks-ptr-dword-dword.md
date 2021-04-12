---
description: 從檔案載入材質，並在完成時以非同步方式通知主機。
MS-HAID: vspixengine.IPixEngine5\_LoadTextureFromFileAsync\_BSTR\_BSTR\_IPixEngine5Callbacks\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixEngine5：： LoadTextureFromFileAsync 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: DF10C209-B6B5-4692-81D7-7FD59CE49F56
api_name:
- IPixEngine5.LoadTextureFromFileAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bef4e4e5117680f7c18f13cc99f801c8e8b8bdfd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109753"
---
# <a name="span-idvspixengineipixengine5_loadtexturefromfileasync_bstr_bstr_ipixengine5callbacks_ptr_dword_dwordspanipixengine5loadtexturefromfileasync-method"></a><span data-ttu-id="54889-103"><span id="vspixengine.ipixengine5_loadtexturefromfileasync_bstr_bstr_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5：： LoadTextureFromFileAsync 方法</span><span class="sxs-lookup"><span data-stu-id="54889-103"><span id="vspixengine.ipixengine5_loadtexturefromfileasync_bstr_bstr_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5::LoadTextureFromFileAsync method</span></span>

<span data-ttu-id="54889-104">從檔案載入材質，並在完成時以非同步方式通知主機。</span><span class="sxs-lookup"><span data-stu-id="54889-104">Loads a texture from a file and notifies the host asynchronously when it completes.</span></span>

## <a name="syntax"></a><span data-ttu-id="54889-105">語法</span><span class="sxs-lookup"><span data-stu-id="54889-105">Syntax</span></span>


```C++
HRESULT LoadTextureFromFileAsync(
   BSTR                  fileName,
   BSTR                  histogramDataFileName,
   IPixEngine5Callbacks* callbacks,
   DWORD                 requestCookie,
   DWORD                 progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="54889-106">參數</span><span class="sxs-lookup"><span data-stu-id="54889-106">Parameters</span></span>

<span data-ttu-id="54889-107">*檔案名* </span><span class="sxs-lookup"><span data-stu-id="54889-107">*fileName* </span></span>  
<span data-ttu-id="54889-108">包含材質檔案名的 COM 字串。</span><span class="sxs-lookup"><span data-stu-id="54889-108">A COM string containing the name of the texture file.</span></span>

<span data-ttu-id="54889-109">*histogramDataFileName* </span><span class="sxs-lookup"><span data-stu-id="54889-109">*histogramDataFileName* </span></span>  
<span data-ttu-id="54889-110">COM 字串，其中包含與材質相關聯的長條圖資料檔案名稱。</span><span class="sxs-lookup"><span data-stu-id="54889-110">A COM string containing the name of the histogram data file associated with the texture.</span></span>

<span data-ttu-id="54889-111">*回檔* </span><span class="sxs-lookup"><span data-stu-id="54889-111">*callbacks* </span></span>  
<span data-ttu-id="54889-112">提供 IPixEngine5 回呼介面之物件的位址。</span><span class="sxs-lookup"><span data-stu-id="54889-112">The address of an object that provides the IPixEngine5 callbacks interface.</span></span>

<span data-ttu-id="54889-113">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="54889-113">*requestCookie* </span></span>  
<span data-ttu-id="54889-114">可唯一 idenfies 要求的 cookie，而且可用來指示它被取消。</span><span class="sxs-lookup"><span data-stu-id="54889-114">A cookie that uniquely idenfies the request, and can be used to signal for it to be canceled.</span></span>

<span data-ttu-id="54889-115">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="54889-115">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="54889-116">未使用。</span><span class="sxs-lookup"><span data-stu-id="54889-116">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="54889-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="54889-117">Return value</span></span>

<span data-ttu-id="54889-118">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="54889-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="54889-119">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="54889-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="54889-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="54889-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="54889-121">標頭</span><span class="sxs-lookup"><span data-stu-id="54889-121">Header</span></span></p></td><td><span data-ttu-id="54889-122">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="54889-122">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="54889-123"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="54889-123"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="54889-124">**IPixEngine5**</span><span class="sxs-lookup"><span data-stu-id="54889-124">**IPixEngine5**</span></span>](/windows/desktop/direct3dtools/ipixengine5)

 

 
