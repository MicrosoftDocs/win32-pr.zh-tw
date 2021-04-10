---
description: 判斷輸入裝置是否支援多點觸控。
ms.assetid: 4fef7060-2235-4bee-a37b-40d827732b30
title: ITablet3：： IsMultiTouch 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet3.IsMultiTouch
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: ed05e110c13af8fe73eebf004183de42eb9fffd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194414"
---
# <a name="itablet3ismultitouch-method"></a><span data-ttu-id="55ba5-103">ITablet3：： IsMultiTouch 方法</span><span class="sxs-lookup"><span data-stu-id="55ba5-103">ITablet3::IsMultiTouch method</span></span>

<span data-ttu-id="55ba5-104">判斷輸入裝置是否支援多點觸控。</span><span class="sxs-lookup"><span data-stu-id="55ba5-104">Determines whether an input device supports multitouch.</span></span>

## <a name="syntax"></a><span data-ttu-id="55ba5-105">語法</span><span class="sxs-lookup"><span data-stu-id="55ba5-105">Syntax</span></span>


```C++
HRESULT IsMultiTouch(
  [out] BOOL *bIsMultiTouch
);
```



## <a name="parameters"></a><span data-ttu-id="55ba5-106">參數</span><span class="sxs-lookup"><span data-stu-id="55ba5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55ba5-107">*bIsMultiTouch* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="55ba5-107">*bIsMultiTouch* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="55ba5-108">指出裝置是否為多點觸控。</span><span class="sxs-lookup"><span data-stu-id="55ba5-108">Indicates whether the device is multitouch.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55ba5-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="55ba5-109">Return value</span></span>

<span data-ttu-id="55ba5-110">成功 **時 \_ 傳回** ，否則 **\_ 會** 傳回錯誤碼，例如 E。</span><span class="sxs-lookup"><span data-stu-id="55ba5-110">Returns **S\_OK** on success, otherwise returns an error code such as **E\_FAIL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="55ba5-111">備註</span><span class="sxs-lookup"><span data-stu-id="55ba5-111">Remarks</span></span>

<span data-ttu-id="55ba5-112">在透過 [**IRealTimeStylus3：： MultiTouchEnabled**](/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus3-get_multitouchenabled) 或 **ITablet3：： IsMultiTouch** 判斷是否有多點觸控功能之後，應用程式可能會加入宣告多點觸控輸入訊息。</span><span class="sxs-lookup"><span data-stu-id="55ba5-112">After determining through [**IRealTimeStylus3::MultiTouchEnabled**](/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus3-get_multitouchenabled) or **ITablet3::IsMultiTouch** that multitouch is available, an application may choose to opt in for multitouch input messages.</span></span> <span data-ttu-id="55ba5-113">您可以在 **IRealTimeStylus3：： MultiTouchEnabled** 屬性區段中找到篩選多點觸控方法的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="55ba5-113">Additional information on filtering multitouch methods is available in the **IRealTimeStylus3::MultiTouchEnabled** property section.</span></span>

## <a name="examples"></a><span data-ttu-id="55ba5-114">範例</span><span class="sxs-lookup"><span data-stu-id="55ba5-114">Examples</span></span>


```C++
CComQIPtr<ITablet3> spITablet3 = g_spITablet3;
VARIANT_BOOL b;
spITablet3->get_IsMultiTouch(&b);
```



## <a name="requirements"></a><span data-ttu-id="55ba5-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="55ba5-115">Requirements</span></span>



| <span data-ttu-id="55ba5-116">需求</span><span class="sxs-lookup"><span data-stu-id="55ba5-116">Requirement</span></span> | <span data-ttu-id="55ba5-117">值</span><span class="sxs-lookup"><span data-stu-id="55ba5-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="55ba5-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="55ba5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="55ba5-119">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="55ba5-119">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="55ba5-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="55ba5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="55ba5-121">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="55ba5-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="55ba5-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="55ba5-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="55ba5-123"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="55ba5-123"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55ba5-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="55ba5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55ba5-125">**ITablet3**</span><span class="sxs-lookup"><span data-stu-id="55ba5-125">**ITablet3**</span></span>](itablet3.md)
</dt> <dt>

[<span data-ttu-id="55ba5-126">**MultiTouchEnabled**</span><span class="sxs-lookup"><span data-stu-id="55ba5-126">**MultiTouchEnabled**</span></span>](/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus3-get_multitouchenabled)
</dt> </dl>

 

 




