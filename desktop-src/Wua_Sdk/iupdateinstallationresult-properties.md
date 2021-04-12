---
description: IUpdateInstallationResult 介面會定義下列屬性。
ms.assetid: 7e8f7125-f89b-416f-bcc5-422eecabe0c4
title: IUpdateInstallationResult 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27b2e2792215d8d927d6e6157c82e37193e74d2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191474"
---
# <a name="iupdateinstallationresult-properties"></a><span data-ttu-id="ec563-103">IUpdateInstallationResult 屬性</span><span class="sxs-lookup"><span data-stu-id="ec563-103">IUpdateInstallationResult Properties</span></span>

<span data-ttu-id="ec563-104">[**IUpdateInstallationResult**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstallationresult)介面會定義下列屬性。</span><span class="sxs-lookup"><span data-stu-id="ec563-104">The [**IUpdateInstallationResult**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstallationresult) interface defines the following properties.</span></span>



| <span data-ttu-id="ec563-105">屬性</span><span class="sxs-lookup"><span data-stu-id="ec563-105">Property</span></span>                                                           | <span data-ttu-id="ec563-106">描述</span><span class="sxs-lookup"><span data-stu-id="ec563-106">Description</span></span>                                                                                                                       |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ec563-107">**HResult**</span><span class="sxs-lookup"><span data-stu-id="ec563-107">**HResult**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstallationresult-get_hresult)               | <span data-ttu-id="ec563-108">取得在更新作業期間引發的 **HRESULT** 例外狀況值。</span><span class="sxs-lookup"><span data-stu-id="ec563-108">Gets the **HRESULT** exception value that is raised during the operation on an update.</span></span>                                            |
| [<span data-ttu-id="ec563-109">**RebootRequired**</span><span class="sxs-lookup"><span data-stu-id="ec563-109">**RebootRequired**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstallationresult-get_rebootrequired) | <span data-ttu-id="ec563-110">取得布林值，指出電腦上是否需要重新開機系統才能完成更新的安裝。</span><span class="sxs-lookup"><span data-stu-id="ec563-110">Gets a Boolean value that indicates whether a system restart is required on a computer to complete the installation of an update.</span></span> |
| [<span data-ttu-id="ec563-111">**ResultCode**</span><span class="sxs-lookup"><span data-stu-id="ec563-111">**ResultCode**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstallationresult-get_resultcode)         | <span data-ttu-id="ec563-112">取得 [**OperationResultCode**](/windows/win32/api/wuapi/ne-wuapi-operationresultcode) 值，這個值會指定更新的作業結果。</span><span class="sxs-lookup"><span data-stu-id="ec563-112">Gets an [**OperationResultCode**](/windows/win32/api/wuapi/ne-wuapi-operationresultcode) value that specifies the result of an operation on an update.</span></span>          |



 

 

 



