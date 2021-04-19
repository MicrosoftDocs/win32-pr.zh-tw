---
title: IConfigAsfWriter GetCurrentProfile 方法
description: GetCurrentProfile 方法會抓取應用程式定義的設定檔。
ms.assetid: 7f6e7085-982b-4234-b890-950efdcdb559
keywords:
- GetCurrentProfile 方法 windows Media 格式
- GetCurrentProfile 方法 windows Media Format，IConfigAsfWriter 介面
- IConfigAsfWriter 介面 windows Media Format，GetCurrentProfile 方法
topic_type:
- apiref
api_name:
- IConfigAsfWriter.GetCurrentProfile
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 88931d83674ffa84288b4bec10e3c9dba15c812a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106969910"
---
# <a name="iconfigasfwritergetcurrentprofile-method"></a><span data-ttu-id="93bee-106">IConfigAsfWriter：： GetCurrentProfile 方法</span><span class="sxs-lookup"><span data-stu-id="93bee-106">IConfigAsfWriter::GetCurrentProfile method</span></span>

<span data-ttu-id="93bee-107">**GetCurrentProfile** 方法會抓取應用程式定義的設定檔。</span><span class="sxs-lookup"><span data-stu-id="93bee-107">The **GetCurrentProfile** method retrieves the application-defined profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="93bee-108">語法</span><span class="sxs-lookup"><span data-stu-id="93bee-108">Syntax</span></span>


```C++
HRESULT GetCurrentProfile(
  [out] IWMProfile **ppProfile
);
```



## <a name="parameters"></a><span data-ttu-id="93bee-109">參數</span><span class="sxs-lookup"><span data-stu-id="93bee-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93bee-110">*ppProfile* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="93bee-110">*ppProfile* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="93bee-111">接收應用程式定義設定檔之 [**IWMProfile**](iwmprofile.md) 介面的指標位址。</span><span class="sxs-lookup"><span data-stu-id="93bee-111">Address of a pointer that receives the [**IWMProfile**](iwmprofile.md) interface of the application-defined profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93bee-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="93bee-112">Return value</span></span>

<span data-ttu-id="93bee-113">如果方法成功，它會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="93bee-113">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="93bee-114">如果失敗，則會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="93bee-114">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="93bee-115">備註</span><span class="sxs-lookup"><span data-stu-id="93bee-115">Remarks</span></span>

<span data-ttu-id="93bee-116">如果方法成功，則傳回的 **IWMProfile** 指標有未處理的參考計數。</span><span class="sxs-lookup"><span data-stu-id="93bee-116">If the method succeeds, the **IWMProfile** pointer that it returns has an outstanding reference count.</span></span> <span data-ttu-id="93bee-117">使用完畢後，請務必釋放介面。</span><span class="sxs-lookup"><span data-stu-id="93bee-117">Be sure to release the interface when you are finished using it.</span></span>

## <a name="see-also"></a><span data-ttu-id="93bee-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="93bee-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="93bee-119">[**IConfigAsfWriter 介面**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="93bee-119">[**IConfigAsfWriter Interface**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span></span>
</dt> </dl>

 

 