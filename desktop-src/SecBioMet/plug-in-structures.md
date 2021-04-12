---
title: 外掛程式結構
description: Windows 生物特徵辨識架構 API 開發用戶端應用程式的結構。
ms.assetid: 64fb908c-72c2-4639-a2f6-77ede080512c
keywords:
- Windows 生物特徵辨識架構 API Windows 生物特徵辨識架構 API、外掛程式結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 193b5a99f30c76e8e6e2ab7ebf0242cf56905816
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301715"
---
# <a name="plug-in-structures"></a><span data-ttu-id="f654c-104">外掛程式結構</span><span class="sxs-lookup"><span data-stu-id="f654c-104">Plug-in Structures</span></span>

<span data-ttu-id="f654c-105">Windows 生物特徵辨識架構 API 開發用戶端應用程式時，支援下列結構。</span><span class="sxs-lookup"><span data-stu-id="f654c-105">The following structures are supported for client application development by the Windows Biometric Framework API.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f654c-106">本節內容</span><span class="sxs-lookup"><span data-stu-id="f654c-106">In this section</span></span>



| <span data-ttu-id="f654c-107">主題</span><span class="sxs-lookup"><span data-stu-id="f654c-107">Topic</span></span>                                                                                                | <span data-ttu-id="f654c-108">描述</span><span class="sxs-lookup"><span data-stu-id="f654c-108">Description</span></span>                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f654c-109">**WINBIO \_ 帳戶 \_ 原則**</span><span class="sxs-lookup"><span data-stu-id="f654c-109">**WINBIO\_ACCOUNT\_POLICY**</span></span>](winbio-account-policy.md)<br/>                                  | <span data-ttu-id="f654c-110">包含預設或帳戶特定的 lnk-antispoofing 原則。</span><span class="sxs-lookup"><span data-stu-id="f654c-110">Contains either a default or account-specific antispoofing policy.</span></span><br/>                                                         |
| [<span data-ttu-id="f654c-111">**WINBIO \_ 介面卡 \_ 介面 \_ 版本**</span><span class="sxs-lookup"><span data-stu-id="f654c-111">**WINBIO\_ADAPTER\_INTERFACE\_VERSION**</span></span>](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_adapter_interface_version)<br/>           | <span data-ttu-id="f654c-112">包含引擎、感應器和儲存介面卡介面資料表中所使用的主要和次要版本號碼。</span><span class="sxs-lookup"><span data-stu-id="f654c-112">Contains a major and minor version number used in the engine, sensor, and storage adapter interface tables.</span></span><br/>                |
| [<span data-ttu-id="f654c-113">**WINBIO \_ 引擎 \_ 介面**</span><span class="sxs-lookup"><span data-stu-id="f654c-113">**WINBIO\_ENGINE\_INTERFACE**</span></span>](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_engine_interface)<br/>                              | <span data-ttu-id="f654c-114">包含自訂引擎介面卡函式的指標。</span><span class="sxs-lookup"><span data-stu-id="f654c-114">Contains pointers to your custom engine adapter functions.</span></span><br/>                                                                 |
| [<span data-ttu-id="f654c-115">**WINBIO \_ 延伸 \_ 註冊 \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="f654c-115">**WINBIO\_EXTENDED\_ENROLLMENT\_PARAMETERS**</span></span>](winbio-extended-enrollment-parameters.md)<br/> | <span data-ttu-id="f654c-116">包含引擎介面卡建立註冊範本時所需的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="f654c-116">Contains additional information that an engine adapter needs to create an enrollment template.</span></span> <br/>                            |
| [<span data-ttu-id="f654c-117">**WINBIO \_ 管線**</span><span class="sxs-lookup"><span data-stu-id="f654c-117">**WINBIO\_PIPELINE**</span></span>](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_pipeline)<br/>                                               | <span data-ttu-id="f654c-118">包含在單一生物特徵辨識裝置中，感應器、引擎和存放裝置介面卡元件所使用的共用內容資訊。</span><span class="sxs-lookup"><span data-stu-id="f654c-118">Contains shared context information used by the sensor, engine, and storage adapter components in a single biometric unit.</span></span><br/> |
| [<span data-ttu-id="f654c-119">**WINBIO \_ 感應器 \_ 介面**</span><span class="sxs-lookup"><span data-stu-id="f654c-119">**WINBIO\_SENSOR\_INTERFACE**</span></span>](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_sensor_interface)<br/>                              | <span data-ttu-id="f654c-120">包含自訂感應器介面卡函式的指標。</span><span class="sxs-lookup"><span data-stu-id="f654c-120">Contains pointers to your custom sensor adapter functions.</span></span><br/>                                                                 |
| [<span data-ttu-id="f654c-121">**WINBIO \_ 儲存體 \_ 介面**</span><span class="sxs-lookup"><span data-stu-id="f654c-121">**WINBIO\_STORAGE\_INTERFACE**</span></span>](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_storage_interface)<br/>                            | <span data-ttu-id="f654c-122">包含您自訂存放裝置介面卡函式的指標。</span><span class="sxs-lookup"><span data-stu-id="f654c-122">Contains pointers to your custom storage adapter functions.</span></span><br/>                                                                |
| [<span data-ttu-id="f654c-123">**WINBIO \_ 儲存體 \_ 記錄**</span><span class="sxs-lookup"><span data-stu-id="f654c-123">**WINBIO\_STORAGE\_RECORD**</span></span>](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_storage_record)<br/>                                  | <span data-ttu-id="f654c-124">包含標準格式的生物特徵辨識範本和相關聯的資料。</span><span class="sxs-lookup"><span data-stu-id="f654c-124">Contains a biometric template and associated data in a standard format.</span></span><br/>                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="f654c-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="f654c-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f654c-126">外掛程式參考</span><span class="sxs-lookup"><span data-stu-id="f654c-126">Plug-in Reference</span></span>](plug-in-reference.md)
</dt> <dt>

[<span data-ttu-id="f654c-127">外掛程式函數</span><span class="sxs-lookup"><span data-stu-id="f654c-127">Plug-in Functions</span></span>](plug-in-functions.md)
</dt> <dt>

[<span data-ttu-id="f654c-128">**WbioQueryEngineInterface**</span><span class="sxs-lookup"><span data-stu-id="f654c-128">**WbioQueryEngineInterface**</span></span>](/windows/desktop/api/Winbio_adapter/nf-winbio_adapter-wbioqueryengineinterface)
</dt> <dt>

[<span data-ttu-id="f654c-129">**WbioQuerySensorInterface**</span><span class="sxs-lookup"><span data-stu-id="f654c-129">**WbioQuerySensorInterface**</span></span>](/windows/desktop/api/Winbio_adapter/nf-winbio_adapter-wbioquerysensorinterface)
</dt> <dt>

[<span data-ttu-id="f654c-130">**WbioQueryStorageInterface**</span><span class="sxs-lookup"><span data-stu-id="f654c-130">**WbioQueryStorageInterface**</span></span>](/windows/desktop/api/Winbio_adapter/nf-winbio_adapter-wbioquerystorageinterface)
</dt> </dl>

 

 





