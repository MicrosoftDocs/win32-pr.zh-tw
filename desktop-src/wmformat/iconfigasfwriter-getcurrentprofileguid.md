---
title: IConfigAsfWriter GetCurrentProfileGuid 方法
description: GetCurrentProfileGuid 方法會抓取目前的 Windows Media system 設定檔 GUID。
ms.assetid: e7a2ecc0-48d4-446c-852a-0d7677cbbe71
keywords:
- GetCurrentProfileGuid 方法 windows Media 格式
- GetCurrentProfileGuid 方法 windows Media Format，IConfigAsfWriter 介面
- IConfigAsfWriter 介面 windows Media Format，GetCurrentProfileGuid 方法
topic_type:
- apiref
api_name:
- IConfigAsfWriter.GetCurrentProfileGuid
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 49282ed6ea33db8052e167568e5b5fa70cda9e01
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316126"
---
# <a name="iconfigasfwritergetcurrentprofileguid-method"></a><span data-ttu-id="e0e4c-106">IConfigAsfWriter：： GetCurrentProfileGuid 方法</span><span class="sxs-lookup"><span data-stu-id="e0e4c-106">IConfigAsfWriter::GetCurrentProfileGuid method</span></span>

<span data-ttu-id="e0e4c-107">**GetCurrentProfileGuid** 方法會抓取目前的 Windows Media system 設定檔 GUID。</span><span class="sxs-lookup"><span data-stu-id="e0e4c-107">The **GetCurrentProfileGuid** method retrieves the current Windows Media system profile GUID.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0e4c-108">語法</span><span class="sxs-lookup"><span data-stu-id="e0e4c-108">Syntax</span></span>


```C++
HRESULT GetCurrentProfileGuid(
  [out] GUID *pProfileGuid
);
```



## <a name="parameters"></a><span data-ttu-id="e0e4c-109">參數</span><span class="sxs-lookup"><span data-stu-id="e0e4c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0e4c-110">*pProfileGuid* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e0e4c-110">*pProfileGuid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e0e4c-111">**GUID** 類型變數的指標，可識別篩選所使用的目前系統設定檔。</span><span class="sxs-lookup"><span data-stu-id="e0e4c-111">Pointer to a variable of type **GUID** that identifies the current system profile being used by the filter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0e4c-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="e0e4c-112">Return value</span></span>

<span data-ttu-id="e0e4c-113">如果方法成功，它會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="e0e4c-113">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="e0e4c-114">如果失敗，則會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="e0e4c-114">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0e4c-115">備註</span><span class="sxs-lookup"><span data-stu-id="e0e4c-115">Remarks</span></span>

<span data-ttu-id="e0e4c-116">這個方法不會與自訂設定檔搭配使用 (包括包含使用 Windows Media 音訊和影片編解碼器) 之資料流程的所有設定檔，因為所有這類設定檔都是由應用程式所建立，而且沒有 GUID 識別碼。</span><span class="sxs-lookup"><span data-stu-id="e0e4c-116">This method is not used with custom profiles (including all profiles that include streams that use the Windows Media Audio and Video codecs) because all such profiles are created by applications and have no GUID identifier.</span></span> <span data-ttu-id="e0e4c-117">如果未載入任何系統設定檔， *pProfileGuid* 會設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="e0e4c-117">If no system profile is loaded, *pProfileGuid* will be set to **NULL**.</span></span>

## <a name="see-also"></a><span data-ttu-id="e0e4c-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e0e4c-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="e0e4c-119">[**IConfigAsfWriter 介面**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e0e4c-119">[**IConfigAsfWriter Interface**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span></span>
</dt> </dl>

 

 