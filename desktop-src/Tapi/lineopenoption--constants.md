---
description: LINEOPENOPTION \_ 常數列出可用來開啟行的選項。
ms.assetid: 361ae90c-a2cf-4107-a2da-80f561a82c56
title: 'LINEOPENOPTION_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dee9182ff7a28627eebd695ce5d9c0877460b15e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997727"
---
# <a name="lineopenoption_-constants"></a><span data-ttu-id="f9d84-103">LINEOPENOPTION \_ 常數</span><span class="sxs-lookup"><span data-stu-id="f9d84-103">LINEOPENOPTION\_ Constants</span></span>

<span data-ttu-id="f9d84-104">**LINEOPENOPTION \_ 常數** 列出可用來開啟行的選項。</span><span class="sxs-lookup"><span data-stu-id="f9d84-104">The **LINEOPENOPTION\_ constants** list the available options for opening a line.</span></span>

<dl> <dt>

<span data-ttu-id="f9d84-105"><span id="LINEOPENOPTION_PROXY"></span><span id="lineopenoption_proxy"></span>**LINEOPENOPTION \_ PROXY**</span><span class="sxs-lookup"><span data-stu-id="f9d84-105"><span id="LINEOPENOPTION_PROXY"></span><span id="lineopenoption_proxy"></span>**LINEOPENOPTION\_PROXY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f9d84-106">應用程式願意處理來自已開啟行之其他應用程式的要求。</span><span class="sxs-lookup"><span data-stu-id="f9d84-106">The application is willing to handle requests from other applications that have the line open.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f9d84-107"><span id="LINEOPENOPTION_SINGLEADDRESS"></span><span id="lineopenoption_singleaddress"></span>**LINEOPENOPTION \_ SINGLEADDRESS**</span><span class="sxs-lookup"><span data-stu-id="f9d84-107"><span id="LINEOPENOPTION_SINGLEADDRESS"></span><span id="lineopenoption_singleaddress"></span>**LINEOPENOPTION\_SINGLEADDRESS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f9d84-108">只有在行裝置上所指定的位址出現在 *lpCallParams* 參數所指向之 [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams)結構的 **dwAddressID** 成員中指定的位址時，應用程式才會收到新呼叫的通知。</span><span class="sxs-lookup"><span data-stu-id="f9d84-108">The application should be informed of new calls created on the line device only if those calls appear on the address specified in the **dwAddressID** member in the [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) structure pointed to by the *lpCallParams* parameter.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f9d84-109">備註</span><span class="sxs-lookup"><span data-stu-id="f9d84-109">Remarks</span></span>

<span data-ttu-id="f9d84-110">如需這些選項的詳細資訊，請參閱 [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) 。</span><span class="sxs-lookup"><span data-stu-id="f9d84-110">See [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) for further details on the operation of these options.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9d84-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="f9d84-111">Requirements</span></span>



| <span data-ttu-id="f9d84-112">需求</span><span class="sxs-lookup"><span data-stu-id="f9d84-112">Requirement</span></span> | <span data-ttu-id="f9d84-113">值</span><span class="sxs-lookup"><span data-stu-id="f9d84-113">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="f9d84-114">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="f9d84-114">TAPI version</span></span><br/> | <span data-ttu-id="f9d84-115">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="f9d84-115">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="f9d84-116">標頭</span><span class="sxs-lookup"><span data-stu-id="f9d84-116">Header</span></span><br/>       | <dl> <span data-ttu-id="f9d84-117"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="f9d84-117"><dt>Tapi.h</dt></span></span> </dl> |



 

 




