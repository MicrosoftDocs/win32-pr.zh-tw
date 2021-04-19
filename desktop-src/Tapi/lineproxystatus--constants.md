---
description: LINEPROXYSTATUS \_ 常數會在應用程式目前開啟的行上指出 proxy 的狀態。
ms.assetid: a5cf3512-ee42-4f64-8fe3-73a14589f78c
title: 'LINEPROXYSTATUS_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e21eaf2708b92448c877230a3be82a6003c9ad9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000909"
---
# <a name="lineproxystatus_-constants"></a><span data-ttu-id="6c838-103">LINEPROXYSTATUS \_ 常數</span><span class="sxs-lookup"><span data-stu-id="6c838-103">LINEPROXYSTATUS\_ Constants</span></span>

<span data-ttu-id="6c838-104">**LINEPROXYSTATUS \_ 常數** 會在應用程式目前開啟的行上指出 proxy 的狀態。</span><span class="sxs-lookup"><span data-stu-id="6c838-104">The **LINEPROXYSTATUS\_ constants** indicate the status of the proxy on a line that the application currently has open.</span></span>

<span data-ttu-id="6c838-105">如需所有可能的 proxy 要求值的清單和描述，請參閱 [**LINEPROXYREQUEST \_ 常數**](lineproxyrequest--constants.md) 。</span><span class="sxs-lookup"><span data-stu-id="6c838-105">See [**LINEPROXYREQUEST\_ Constants**](lineproxyrequest--constants.md) for a list and description of all possible proxy request values.</span></span>

<dl> <dt>

<span data-ttu-id="6c838-106"><span id="LINEPROXYSTATUS_ALLOPENFORACD"></span><span id="lineproxystatus_allopenforacd"></span>**LINEPROXYSTATUS \_ ALLOPENFORACD**</span><span class="sxs-lookup"><span data-stu-id="6c838-106"><span id="LINEPROXYSTATUS_ALLOPENFORACD"></span><span id="lineproxystatus_allopenforacd"></span>**LINEPROXYSTATUS\_ALLOPENFORACD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6c838-107">這一行現在已針對 TAPI 3.0 版和更新版本 ACD 作業所需的所有 proxy 要求類型開啟 proxy。</span><span class="sxs-lookup"><span data-stu-id="6c838-107">The line now has proxies open for all the proxy request types required for ACD operations by TAPI version 3.0 and higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c838-108"><span id="LINEPROXYSTATUS_CLOSE"></span><span id="lineproxystatus_close"></span>**LINEPROXYSTATUS \_ 關閉**</span><span class="sxs-lookup"><span data-stu-id="6c838-108"><span id="LINEPROXYSTATUS_CLOSE"></span><span id="lineproxystatus_close"></span>**LINEPROXYSTATUS\_CLOSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6c838-109">Proxy 已關閉。</span><span class="sxs-lookup"><span data-stu-id="6c838-109">A proxy has closed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6c838-110"><span id="LINEPROXYSTATUS_OPEN"></span><span id="lineproxystatus_open"></span>**LINEPROXYSTATUS \_ 開啟**</span><span class="sxs-lookup"><span data-stu-id="6c838-110"><span id="LINEPROXYSTATUS_OPEN"></span><span id="lineproxystatus_open"></span>**LINEPROXYSTATUS\_OPEN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6c838-111">已開啟新的 proxy。</span><span class="sxs-lookup"><span data-stu-id="6c838-111">A new proxy has opened.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6c838-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="6c838-112">Requirements</span></span>



| <span data-ttu-id="6c838-113">需求</span><span class="sxs-lookup"><span data-stu-id="6c838-113">Requirement</span></span> | <span data-ttu-id="6c838-114">值</span><span class="sxs-lookup"><span data-stu-id="6c838-114">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="6c838-115">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="6c838-115">TAPI version</span></span><br/> | <span data-ttu-id="6c838-116">需要 TAPI 2。2</span><span class="sxs-lookup"><span data-stu-id="6c838-116">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="6c838-117">標頭</span><span class="sxs-lookup"><span data-stu-id="6c838-117">Header</span></span><br/>       | <dl> <span data-ttu-id="6c838-118"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="6c838-118"><dt>Tapi.h</dt></span></span> </dl> |



 

 




