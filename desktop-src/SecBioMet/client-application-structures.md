---
title: 用戶端應用程式結構
description: Windows 生物特徵辨識架構 API 所支援的用戶端應用程式開發結構。
ms.assetid: ac13910c-0c33-4fb8-a9c6-a2d5b1b28c73
keywords:
- Windows 生物特徵辨識架構 API Windows 生物特徵辨識架構 API、用戶端應用程式結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3e04de50fb340c4acf7e66b4e6154f2176a7adb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675152"
---
# <a name="client-application-structures"></a><span data-ttu-id="65f11-104">用戶端應用程式結構</span><span class="sxs-lookup"><span data-stu-id="65f11-104">Client Application Structures</span></span>

<span data-ttu-id="65f11-105">Windows 生物特徵辨識架構 API 開發用戶端應用程式時，支援下列結構。</span><span class="sxs-lookup"><span data-stu-id="65f11-105">The following structures are supported for client application development by the Windows Biometric Framework API.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="65f11-106">本節內容</span><span class="sxs-lookup"><span data-stu-id="65f11-106">In this section</span></span>



| <span data-ttu-id="65f11-107">主題</span><span class="sxs-lookup"><span data-stu-id="65f11-107">Topic</span></span>                                                                                        | <span data-ttu-id="65f11-108">描述</span><span class="sxs-lookup"><span data-stu-id="65f11-108">Description</span></span>                                                                                                                     |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="65f11-109">**WINBIO \_ 反 \_ 詐騙 \_ 原則**</span><span class="sxs-lookup"><span data-stu-id="65f11-109">**WINBIO\_ANTI\_SPOOF\_POLICY**</span></span>](winbio-anti-spoof-policy.md)<br/>                   | <span data-ttu-id="65f11-110">表示使用者的 lnk-antispoofing 原則。</span><span class="sxs-lookup"><span data-stu-id="65f11-110">Represents the antispoofing policy for a user.</span></span><br/>                                                                       |
| [<span data-ttu-id="65f11-111">**WINBIO \_ 非同步 \_ 結果**</span><span class="sxs-lookup"><span data-stu-id="65f11-111">**WINBIO\_ASYNC\_RESULT**</span></span>](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result)<br/>                              | <span data-ttu-id="65f11-112">包含非同步作業的結果。</span><span class="sxs-lookup"><span data-stu-id="65f11-112">Contains the results of an asynchronous operation.</span></span><br/>                                                                   |
| [<span data-ttu-id="65f11-113">**WINBIO \_ BDB \_ ANSI \_ 381 \_ 標頭**</span><span class="sxs-lookup"><span data-stu-id="65f11-113">**WINBIO\_BDB\_ANSI\_381\_HEADER**</span></span>](winbio-bdb-ansi-381-header.md)<br/>              | <span data-ttu-id="65f11-114">指定一系列指紋或棕櫚範例的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="65f11-114">Specifies information about a series of fingerprint or palm samples.</span></span><br/>                                                 |
| [<span data-ttu-id="65f11-115">**WINBIO \_ BDB \_ ANSI \_ 381 \_ 記錄**</span><span class="sxs-lookup"><span data-stu-id="65f11-115">**WINBIO\_BDB\_ANSI\_381\_RECORD**</span></span>](winbio-bdb-ansi-381-record.md)<br/>              | <span data-ttu-id="65f11-116">包含來自終端使用者的單一指紋或棕櫚範例的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="65f11-116">Contains information about a single fingerprint or palm sample from an end user.</span></span><br/>                                     |
| [<span data-ttu-id="65f11-117">**WINBIO \_ BIR**</span><span class="sxs-lookup"><span data-stu-id="65f11-117">**WINBIO\_BIR**</span></span>](winbio-bir.md)<br/>                                                 | <span data-ttu-id="65f11-118">代表 (BIR) 的生物特徵辨識資訊記錄。</span><span class="sxs-lookup"><span data-stu-id="65f11-118">Represents a biometric information record (BIR).</span></span><br/>                                                                     |
| [<span data-ttu-id="65f11-119">**WINBIO \_ BIR \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="65f11-119">**WINBIO\_BIR\_DATA**</span></span>](winbio-bir-data.md)<br/>                                      | <span data-ttu-id="65f11-120">指定生物特徵辨識資訊區塊的大小（以位元組為單位）和位移。</span><span class="sxs-lookup"><span data-stu-id="65f11-120">Specifies the size, in bytes, and the offset of a block of biometric information.</span></span><br/>                                    |
| [<span data-ttu-id="65f11-121">**WINBIO \_ BIR \_ 標頭**</span><span class="sxs-lookup"><span data-stu-id="65f11-121">**WINBIO\_BIR\_HEADER**</span></span>](winbio-bir-header.md)<br/>                                  | <span data-ttu-id="65f11-122">包含 (BIR) 的生物特徵辨識資訊記錄標頭。</span><span class="sxs-lookup"><span data-stu-id="65f11-122">Contains the header of a biometric information record (BIR).</span></span><br/>                                                         |
| [<span data-ttu-id="65f11-123">**WINBIO \_ BSP \_ 架構**</span><span class="sxs-lookup"><span data-stu-id="65f11-123">**WINBIO\_BSP\_SCHEMA**</span></span>](winbio-bsp-schema.md)<br/>                                  | <span data-ttu-id="65f11-124">描述生物特徵辨識服務提供者的功能。</span><span class="sxs-lookup"><span data-stu-id="65f11-124">Describes the capabilities of a biometric service provider.</span></span><br/>                                                          |
| [<span data-ttu-id="65f11-125">**WINBIO \_ 延伸 \_ 引擎 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="65f11-125">**WINBIO\_EXTENDED\_ENGINE\_INFO**</span></span>](winbio-extended-engine-info.md)<br/>             | <span data-ttu-id="65f11-126">包含生物特徵辨識裝置引擎介面卡的功能和註冊需求相關資訊。</span><span class="sxs-lookup"><span data-stu-id="65f11-126">Contains information about the capabilities and enrollment requirements of the engine adapter for a biometric unit.</span></span><br/>  |
| [<span data-ttu-id="65f11-127">**WINBIO \_ 延伸 \_ 註冊 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="65f11-127">**WINBIO\_EXTENDED\_ENROLLMENT\_STATUS**</span></span>](winbio-extended-enrollment-status.md)<br/> | <span data-ttu-id="65f11-128">包含正在進行中之註冊狀態的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="65f11-128">Contains additional information about the status of an enrollment that is in progress.</span></span><br/>                               |
| [<span data-ttu-id="65f11-129">**WINBIO \_ 擴充的 \_ 感應器 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="65f11-129">**WINBIO\_EXTENDED\_SENSOR\_INFO**</span></span>](winbio-extended-sensor-info.md)<br/>             | <span data-ttu-id="65f11-130">包含生物特徵辨識設備之感應器介面卡的功能和註冊需求相關資訊。</span><span class="sxs-lookup"><span data-stu-id="65f11-130">Contains information about the capabilities and enrollment requirements of the sensor adapter for a biometric unit.</span></span><br/>  |
| [<span data-ttu-id="65f11-131">**WINBIO \_ 延伸 \_ 儲存體 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="65f11-131">**WINBIO\_EXTENDED\_STORAGE\_INFO**</span></span>](winbio-extended-storage-info.md)<br/>           | <span data-ttu-id="65f11-132">包含生物識別設備之儲存體介面卡的功能和註冊需求相關資訊。</span><span class="sxs-lookup"><span data-stu-id="65f11-132">Contains information about the capabilities and enrollment requirements of the storage adapter for a biometric unit.</span></span><br/> |
| [<span data-ttu-id="65f11-133">**WINBIO \_ 事件**</span><span class="sxs-lookup"><span data-stu-id="65f11-133">**WINBIO\_EVENT**</span></span>](winbio-event.md)<br/>                                             | <span data-ttu-id="65f11-134">包含引發事件通知時，傳送至回呼常式的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="65f11-134">Contains status information sent to the callback routine when an event notice is raised.</span></span><br/>                             |
| [<span data-ttu-id="65f11-135">**WINBIO 身分 \_ 識別**</span><span class="sxs-lookup"><span data-stu-id="65f11-135">**WINBIO\_IDENTITY**</span></span>](winbio-identity.md)<br/>                                       | <span data-ttu-id="65f11-136">包含與生物識別範本相關聯的識別值。</span><span class="sxs-lookup"><span data-stu-id="65f11-136">Contains an identifying value associated with a biometric template.</span></span><br/>                                                  |
| [<span data-ttu-id="65f11-137">**WINBIO \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="65f11-137">**WINBIO\_PRESENCE**</span></span>](winbio-presence.md)<br/>                                       | <span data-ttu-id="65f11-138">包含正在監視的個人是否存在的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="65f11-138">Contains information about the presence of an individual whose presence is being monitored.</span></span><br/>                          |
| [<span data-ttu-id="65f11-139">**WINBIO \_ 註冊的 \_ 格式**</span><span class="sxs-lookup"><span data-stu-id="65f11-139">**WINBIO\_REGISTERED\_FORMAT**</span></span>](winbio-registered-format.md)<br/>                    | <span data-ttu-id="65f11-140">將已註冊的資料格式指定為擁有者/格式組。</span><span class="sxs-lookup"><span data-stu-id="65f11-140">Specifies a registered data format as an owner/format pair.</span></span><br/>                                                          |
| [<span data-ttu-id="65f11-141">**WINBIO \_ 儲存體 \_ 架構**</span><span class="sxs-lookup"><span data-stu-id="65f11-141">**WINBIO\_STORAGE\_SCHEMA**</span></span>](winbio-storage-schema.md)<br/>                          | <span data-ttu-id="65f11-142">描述生物特徵辨識存儲裝置配接器的功能。</span><span class="sxs-lookup"><span data-stu-id="65f11-142">Describes the capabilities of a biometric storage adapter.</span></span><br/>                                                           |
| [<span data-ttu-id="65f11-143">**WINBIO \_ 單元 \_ 架構**</span><span class="sxs-lookup"><span data-stu-id="65f11-143">**WINBIO\_UNIT\_SCHEMA**</span></span>](winbio-unit-schema.md)<br/>                                | <span data-ttu-id="65f11-144">描述生物特徵辨識設備的功能。</span><span class="sxs-lookup"><span data-stu-id="65f11-144">Describes the capabilities of a biometric unit.</span></span><br/>                                                                      |
| [<span data-ttu-id="65f11-145">**WINBIO \_ 版本**</span><span class="sxs-lookup"><span data-stu-id="65f11-145">**WINBIO\_VERSION**</span></span>](winbio-version.md)<br/>                                         | <span data-ttu-id="65f11-146">包含生物特徵辨識服務提供者元件的軟體版本號碼。</span><span class="sxs-lookup"><span data-stu-id="65f11-146">Contains the software version number of a biometric service provider component.</span></span><br/>                                      |



 

 

 





