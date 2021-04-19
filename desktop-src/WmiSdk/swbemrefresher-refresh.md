---
description: SWbemRefresher 方法會更新 SWbemRefresher 物件中包含的所有專案。SWbemRefresher 物件。
ms.assetid: 85a4777a-4be7-44f2-b7a6-e18b5e57f7af
ms.tgt_platform: multiple
title: 'SWbemRefresher 方法 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.Refresh
- ISWbemRefresher.Refresh
- ISWbemRefresher.Refresh
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: d8b2522227041858770c7256d7d2520cc661948e
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106989115"
---
# <a name="swbemrefresherrefresh-method"></a><span data-ttu-id="df0b1-103">SWbemRefresher 方法</span><span class="sxs-lookup"><span data-stu-id="df0b1-103">SWbemRefresher.Refresh method</span></span>

<span data-ttu-id="df0b1-104">**SWbemRefresher** 方法會更新 [**SWbemRefresher**](swbemrefresher.md)物件中包含的所有專案。</span><span class="sxs-lookup"><span data-stu-id="df0b1-104">The **SWbemRefresher.Refresh** method updates all the items that are contained in the [**SWbemRefresher**](swbemrefresher.md) object.</span></span>

<span data-ttu-id="df0b1-105">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="df0b1-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="df0b1-106">語法</span><span class="sxs-lookup"><span data-stu-id="df0b1-106">Syntax</span></span>


```VB
SWbemRefresher.Refresh( _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="df0b1-107">參數</span><span class="sxs-lookup"><span data-stu-id="df0b1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df0b1-108">*iFlags* \[選\]</span><span class="sxs-lookup"><span data-stu-id="df0b1-108">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="df0b1-109">旗標必須設定為 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="df0b1-109">Flags must be set to 0 (zero).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df0b1-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="df0b1-110">Return value</span></span>

<span data-ttu-id="df0b1-111">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="df0b1-111">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="df0b1-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="df0b1-112">Requirements</span></span>



| <span data-ttu-id="df0b1-113">需求</span><span class="sxs-lookup"><span data-stu-id="df0b1-113">Requirement</span></span> | <span data-ttu-id="df0b1-114">值</span><span class="sxs-lookup"><span data-stu-id="df0b1-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="df0b1-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="df0b1-115">Minimum supported client</span></span><br/> | <span data-ttu-id="df0b1-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="df0b1-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="df0b1-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="df0b1-117">Minimum supported server</span></span><br/> | <span data-ttu-id="df0b1-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="df0b1-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="df0b1-119">標頭</span><span class="sxs-lookup"><span data-stu-id="df0b1-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="df0b1-120"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="df0b1-120"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="df0b1-121">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="df0b1-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="df0b1-122"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="df0b1-122"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="df0b1-123">DLL</span><span class="sxs-lookup"><span data-stu-id="df0b1-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df0b1-124"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df0b1-124"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="df0b1-125">CLSID</span><span class="sxs-lookup"><span data-stu-id="df0b1-125">CLSID</span></span><br/>                    | <span data-ttu-id="df0b1-126">CLSID \_ SWbemRefresher</span><span class="sxs-lookup"><span data-stu-id="df0b1-126">CLSID\_SWbemRefresher</span></span><br/>                                                        |
| <span data-ttu-id="df0b1-127">IID</span><span class="sxs-lookup"><span data-stu-id="df0b1-127">IID</span></span><br/>                      | <span data-ttu-id="df0b1-128">IID \_ ISWbemRefresher</span><span class="sxs-lookup"><span data-stu-id="df0b1-128">IID\_ISWbemRefresher</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="df0b1-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="df0b1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df0b1-130">**SWbemRefresher**</span><span class="sxs-lookup"><span data-stu-id="df0b1-130">**SWbemRefresher**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




