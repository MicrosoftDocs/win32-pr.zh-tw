---
description: 代表檔案歷程記錄重新關聯功能，可讓使用者重新建立與過去相同使用者所使用的備份目標的關聯性。 重新關聯是藉由呼叫 IFhReassociation 介面的方法來執行。
ms.assetid: BB81F8ED-4DFB-4FA5-B3ED-ACBAB32BBE3D
title: 'FhReassociation 類別 (Fhcfg) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FhReassociation
api_type:
- COM
api_location:
- Fhcfg.idl
ms.openlocfilehash: 1e303799a792e788fcb948ad6d3c6e2fd732e26e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986258"
---
# <a name="fhreassociation-class"></a><span data-ttu-id="d3ccf-104">FhReassociation 類別</span><span class="sxs-lookup"><span data-stu-id="d3ccf-104">FhReassociation class</span></span>

<span data-ttu-id="d3ccf-105">代表檔案歷程記錄重新關聯功能，可讓使用者重新建立與過去相同使用者所使用的備份目標的關聯性。</span><span class="sxs-lookup"><span data-stu-id="d3ccf-105">Represents the File History reassociation feature, which allows a user to reestablish a relationship with a backup target that was used by the same user in the past.</span></span> <span data-ttu-id="d3ccf-106">重新關聯是藉由呼叫 [**IFhReassociation**](/windows/desktop/api/Fhcfg/nn-fhcfg-ifhreassociation) 介面的方法來執行。</span><span class="sxs-lookup"><span data-stu-id="d3ccf-106">Reassociation is performed by calling the methods of the [**IFhReassociation**](/windows/desktop/api/Fhcfg/nn-fhcfg-ifhreassociation) interface.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="d3ccf-107">執行時機</span><span class="sxs-lookup"><span data-stu-id="d3ccf-107">When to implement</span></span>

<span data-ttu-id="d3ccf-108">檔案歷程記錄 API 會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="d3ccf-108">The File History API implements this class.</span></span> <span data-ttu-id="d3ccf-109">若要建立這個類別的實例，請使用 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 函數。</span><span class="sxs-lookup"><span data-stu-id="d3ccf-109">To create an instance of this class, use the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3ccf-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="d3ccf-110">Requirements</span></span>



| <span data-ttu-id="d3ccf-111">需求</span><span class="sxs-lookup"><span data-stu-id="d3ccf-111">Requirement</span></span> | <span data-ttu-id="d3ccf-112">值</span><span class="sxs-lookup"><span data-stu-id="d3ccf-112">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d3ccf-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d3ccf-113">Minimum supported client</span></span><br/> | <span data-ttu-id="d3ccf-114">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d3ccf-114">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d3ccf-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d3ccf-115">Minimum supported server</span></span><br/> | <span data-ttu-id="d3ccf-116">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d3ccf-116">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d3ccf-117">標頭</span><span class="sxs-lookup"><span data-stu-id="d3ccf-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3ccf-118"><dt>Fhcfg。h</dt></span><span class="sxs-lookup"><span data-stu-id="d3ccf-118"><dt>Fhcfg.h</dt></span></span> </dl>   |
| <span data-ttu-id="d3ccf-119">Idl</span><span class="sxs-lookup"><span data-stu-id="d3ccf-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d3ccf-120"><dt>Fhcfg .idl</dt></span><span class="sxs-lookup"><span data-stu-id="d3ccf-120"><dt>Fhcfg.idl</dt></span></span> </dl> |



 

 
