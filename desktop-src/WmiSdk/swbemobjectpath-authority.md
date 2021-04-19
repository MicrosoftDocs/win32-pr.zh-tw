---
description: SWbemObjectPath 物件的 [授權] 屬性包含一個字串，該字串會定義物件路徑的授權單位部分。
ms.assetid: f00e5759-03b4-4333-b89e-5f54db73c3b7
ms.tgt_platform: multiple
title: 'SWbemObjectPath 授權屬性 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.Authority
- ISWbemObjectPath.Authority
- ISWbemObjectPath.get_Authority
- ISWbemObjectPath.put_Authority
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c2b452f37f9f8d36b33596e032a82441a3507d42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975932"
---
# <a name="swbemobjectpathauthority-property"></a><span data-ttu-id="fdf1f-103">SWbemObjectPath 授權屬性</span><span class="sxs-lookup"><span data-stu-id="fdf1f-103">SWbemObjectPath.Authority property</span></span>

<span data-ttu-id="fdf1f-104">[**SWbemObjectPath**](swbemobjectpath.md)物件的 [**授權**] 屬性包含一個字串，該字串會定義物件路徑的授權單位部分。</span><span class="sxs-lookup"><span data-stu-id="fdf1f-104">The **Authority** property of the [**SWbemObjectPath**](swbemobjectpath.md) object contains a string that defines the Authority component of the object path.</span></span> <span data-ttu-id="fdf1f-105">如需詳細資訊，請參閱 [**wbemscripting.swbemlocator. ConnectServer**](swbemlocator-connectserver.md)方法的 *strAuthority* 參數，以及 [設定 IWbemServices 和其他 proxy 的安全性](setting-the-security-on-iwbemservices-and-other-proxies.md)。</span><span class="sxs-lookup"><span data-stu-id="fdf1f-105">For more information, see the *strAuthority* parameter of the [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) method and [Setting the Security on IWbemServices and Other Proxies](setting-the-security-on-iwbemservices-and-other-proxies.md).</span></span>

<span data-ttu-id="fdf1f-106">如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。</span><span class="sxs-lookup"><span data-stu-id="fdf1f-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="fdf1f-107">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="fdf1f-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="fdf1f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="fdf1f-108">Syntax</span></span>


```VB
SWbemObjectPath.Authority As String
```



## <a name="property-value"></a><span data-ttu-id="fdf1f-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="fdf1f-109">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="fdf1f-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="fdf1f-110">Requirements</span></span>



| <span data-ttu-id="fdf1f-111">需求</span><span class="sxs-lookup"><span data-stu-id="fdf1f-111">Requirement</span></span> | <span data-ttu-id="fdf1f-112">值</span><span class="sxs-lookup"><span data-stu-id="fdf1f-112">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fdf1f-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fdf1f-113">Minimum supported client</span></span><br/> | <span data-ttu-id="fdf1f-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fdf1f-114">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fdf1f-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fdf1f-115">Minimum supported server</span></span><br/> | <span data-ttu-id="fdf1f-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fdf1f-116">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fdf1f-117">標頭</span><span class="sxs-lookup"><span data-stu-id="fdf1f-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="fdf1f-118"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="fdf1f-118"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="fdf1f-119">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="fdf1f-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="fdf1f-120"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="fdf1f-120"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="fdf1f-121">DLL</span><span class="sxs-lookup"><span data-stu-id="fdf1f-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fdf1f-122"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fdf1f-122"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="fdf1f-123">CLSID</span><span class="sxs-lookup"><span data-stu-id="fdf1f-123">CLSID</span></span><br/>                    | <span data-ttu-id="fdf1f-124">CLSID \_ SWbemObjectPath</span><span class="sxs-lookup"><span data-stu-id="fdf1f-124">CLSID\_SWbemObjectPath</span></span><br/>                                                       |
| <span data-ttu-id="fdf1f-125">IID</span><span class="sxs-lookup"><span data-stu-id="fdf1f-125">IID</span></span><br/>                      | <span data-ttu-id="fdf1f-126">IID \_ ISWbemObjectPath</span><span class="sxs-lookup"><span data-stu-id="fdf1f-126">IID\_ISWbemObjectPath</span></span><br/>                                                        |



 

 




