---
description: IInstallationResult 介面會定義下列屬性。
ms.assetid: bd6cd5ae-2e43-4ac3-8ce7-ac80b7fc5cb8
title: IInstallationResult 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78783b6758ab30d6a77c07cd71111486f3a7343e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026278"
---
# <a name="iinstallationresult-properties"></a><span data-ttu-id="8eac6-103">IInstallationResult 屬性</span><span class="sxs-lookup"><span data-stu-id="8eac6-103">IInstallationResult Properties</span></span>

<span data-ttu-id="8eac6-104">[**IInstallationResult**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationresult)介面會定義下列屬性。</span><span class="sxs-lookup"><span data-stu-id="8eac6-104">The [**IInstallationResult**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationresult) interface defines the following properties.</span></span>



| <span data-ttu-id="8eac6-105">屬性</span><span class="sxs-lookup"><span data-stu-id="8eac6-105">Property</span></span>                                                     | <span data-ttu-id="8eac6-106">描述</span><span class="sxs-lookup"><span data-stu-id="8eac6-106">Description</span></span>                                                                                                                            |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8eac6-107">**HResult**</span><span class="sxs-lookup"><span data-stu-id="8eac6-107">**HResult**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationresult-get_hresult)               | <span data-ttu-id="8eac6-108">取得安裝期間引發之例外狀況的 **HRESULT** （如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="8eac6-108">Gets the **HRESULT** of the exception, if any, that is raised during the installation.</span></span>                                                 |
| [<span data-ttu-id="8eac6-109">**RebootRequired**</span><span class="sxs-lookup"><span data-stu-id="8eac6-109">**RebootRequired**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationresult-get_rebootrequired) | <span data-ttu-id="8eac6-110">取得布林值，指出您是否必須重新開機電腦，才能完成安裝或卸載更新。</span><span class="sxs-lookup"><span data-stu-id="8eac6-110">Gets a Boolean value that indicates whether you must restart the computer to complete the installation or uninstallation of an update.</span></span> |
| [<span data-ttu-id="8eac6-111">**ResultCode**</span><span class="sxs-lookup"><span data-stu-id="8eac6-111">**ResultCode**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationresult-get_resultcode)         | <span data-ttu-id="8eac6-112">取得 [**OperationResultCode**](/windows/win32/api/wuapi/ne-wuapi-operationresultcode) 值，這個值會指定更新的作業結果。</span><span class="sxs-lookup"><span data-stu-id="8eac6-112">Gets an [**OperationResultCode**](/windows/win32/api/wuapi/ne-wuapi-operationresultcode) value that specifies the result of an operation on an update.</span></span>               |



 

 

 



