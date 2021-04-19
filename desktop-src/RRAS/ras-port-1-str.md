---
title: 'RAS_PORT_1 結構 (Rassapi .h) '
description: RAS \_ 埠 \_ 1 結構包含 ras 埠的相關資訊。
ms.assetid: f226ef16-feb4-41e0-ba60-ddb2f0acd305
keywords:
- RAS_PORT_1 結構 RAS
- PRAS_PORT_1 結構指標 RAS
topic_type:
- apiref
api_name:
- RAS_PORT_1
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d73fe450e5ea5f8ceee48436dbbe05570d0d818a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966932"
---
# <a name="ras_port_1-structure"></a><span data-ttu-id="6e0c8-105">RAS \_ 埠 \_ 1 結構</span><span class="sxs-lookup"><span data-stu-id="6e0c8-105">RAS\_PORT\_1 structure</span></span>

<span data-ttu-id="6e0c8-106">\[Windows Vista 不支援這個版本的 **RAS \_ 埠 \_ 1** 結構。</span><span class="sxs-lookup"><span data-stu-id="6e0c8-106">\[This version of the **RAS\_PORT\_1** structure is not supported as of Windows Vista.</span></span> <span data-ttu-id="6e0c8-107">請改用 mprapi 中定義的較新 [**RAS \_ 埠 \_ 1**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_1) 。\]</span><span class="sxs-lookup"><span data-stu-id="6e0c8-107">Use the newer [**RAS\_PORT\_1**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_1) defined in mprapi.h instead.\]</span></span>

<span data-ttu-id="6e0c8-108">**Ras \_ 埠 \_ 1** 結構包含 ras 埠的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="6e0c8-108">The **RAS\_PORT\_1** structure contains information about a RAS port.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e0c8-109">語法</span><span class="sxs-lookup"><span data-stu-id="6e0c8-109">Syntax</span></span>


```C++
typedef struct _RAS_PORT_1 {
  RAS_PORT_0                rasport0;
  DWORD                     LineCondition;
  DWORD                     HardwareCondition;
  DWORD                     LineSpeed;
  WORD                      NumStatistics;
  WORD                      NumMediaParms;
  DWORD                     SizeMediaParms;
  RAS_PPP_PROJECTION_RESULT ProjResult;
} RAS_PORT_1, *PRAS_PORT_1;
```



## <a name="members"></a><span data-ttu-id="6e0c8-110">成員</span><span class="sxs-lookup"><span data-stu-id="6e0c8-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="6e0c8-111">**rasport0**</span><span class="sxs-lookup"><span data-stu-id="6e0c8-111">**rasport0**</span></span>
</dt> <dd>

<span data-ttu-id="6e0c8-112">指定包含埠相關資訊的 [**RAS \_ 埠 \_ 0**](ras-port-0-str.md) 結構，例如埠的名稱、連接到埠的遠端使用者名稱等等。</span><span class="sxs-lookup"><span data-stu-id="6e0c8-112">Specifies a [**RAS\_PORT\_0**](ras-port-0-str.md) structure that contains information about the port, such as the name of the port, the name of the remote user connected to the port, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="6e0c8-113">**LineCondition**</span><span class="sxs-lookup"><span data-stu-id="6e0c8-113">**LineCondition**</span></span>
</dt> <dd>

<span data-ttu-id="6e0c8-114">指定埠的狀態。</span><span class="sxs-lookup"><span data-stu-id="6e0c8-114">Specifies the state of the port.</span></span> <span data-ttu-id="6e0c8-115">這個成員可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="6e0c8-115">This member can be one of the following values.</span></span>



| <span data-ttu-id="6e0c8-116">值</span><span class="sxs-lookup"><span data-stu-id="6e0c8-116">Value</span></span>                                                                                                                                                                                            | <span data-ttu-id="6e0c8-117">意義</span><span class="sxs-lookup"><span data-stu-id="6e0c8-117">Meaning</span></span>                                                                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RAS_PORT_NON_OPERATIONAL"></span><span id="ras_port_non_operational"></span><dl> <span data-ttu-id="6e0c8-118"><dt>**RAS \_ 埠 \_ 無法 \_ 運作**</dt></span><span class="sxs-lookup"><span data-stu-id="6e0c8-118"><dt>**RAS\_PORT\_NON\_OPERATIONAL**</dt></span></span> </dl> | <span data-ttu-id="6e0c8-119">埠無法運作。</span><span class="sxs-lookup"><span data-stu-id="6e0c8-119">The port is not operational.</span></span> <span data-ttu-id="6e0c8-120">檢查事件記錄檔中是否有伺服器回報的錯誤。</span><span class="sxs-lookup"><span data-stu-id="6e0c8-120">Check the event log for errors reported by the server.</span></span><br/>                                                                         |
| <span id="RAS_PORT_DISCONNECTED"></span><span id="ras_port_disconnected"></span><dl> <span data-ttu-id="6e0c8-121"><dt>**RAS \_ 埠已 \_ 中斷連線**</dt></span><span class="sxs-lookup"><span data-stu-id="6e0c8-121"><dt>**RAS\_PORT\_DISCONNECTED**</dt></span></span> </dl>           | <span data-ttu-id="6e0c8-122">埠目前已中斷連線。</span><span class="sxs-lookup"><span data-stu-id="6e0c8-122">The port is currently disconnected.</span></span><br/>                                                                                                                         |
| <span id="RAS_PORT_CALLING_BACK"></span><span id="ras_port_calling_back"></span><dl> <span data-ttu-id="6e0c8-123"><dt>**RAS \_ 埠 \_ 回呼 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6e0c8-123"><dt>**RAS\_PORT\_CALLING\_BACK**</dt></span></span> </dl>          | <span data-ttu-id="6e0c8-124">RAS 伺服器正在回呼 RAS 用戶端。</span><span class="sxs-lookup"><span data-stu-id="6e0c8-124">The RAS server is calling back the RAS client.</span></span><br/>                                                                                                              |
| <span id="RAS_PORT_LISTENING"></span><span id="ras_port_listening"></span><dl> <span data-ttu-id="6e0c8-125"><dt>**RAS \_ 埠 \_ 接聽**</dt></span><span class="sxs-lookup"><span data-stu-id="6e0c8-125"><dt>**RAS\_PORT\_LISTENING**</dt></span></span> </dl>                    | <span data-ttu-id="6e0c8-126">埠正在等候用戶端在中呼叫。</span><span class="sxs-lookup"><span data-stu-id="6e0c8-126">The port is waiting for a client to call in.</span></span><br/>                                                                                                                |
| <span id="RAS_PORT_AUTHENTICATING"></span><span id="ras_port_authenticating"></span><dl> <span data-ttu-id="6e0c8-127"><dt>**RAS \_ 埠 \_ 驗證**</dt></span><span class="sxs-lookup"><span data-stu-id="6e0c8-127"><dt>**RAS\_PORT\_AUTHENTICATING**</dt></span></span> </dl>     | <span data-ttu-id="6e0c8-128">伺服器正在驗證遠端用戶端。</span><span class="sxs-lookup"><span data-stu-id="6e0c8-128">The server is in the process of authenticating the remote client.</span></span><br/>                                                                                           |
| <span id="RAS_PORT_AUTHENTICATED"></span><span id="ras_port_authenticated"></span><dl> <span data-ttu-id="6e0c8-129"><dt>**\_ \_ 已驗證的 RAS 埠**</dt></span><span class="sxs-lookup"><span data-stu-id="6e0c8-129"><dt>**RAS\_PORT\_AUTHENTICATED**</dt></span></span> </dl>        | <span data-ttu-id="6e0c8-130">遠端用戶端現在已經過驗證。</span><span class="sxs-lookup"><span data-stu-id="6e0c8-130">The remote client is now authenticated.</span></span><br/>                                                                                                                     |
| <span id="RAS_PORT_INITIALIZING"></span><span id="ras_port_initializing"></span><dl> <span data-ttu-id="6e0c8-131"><dt>**RAS \_ 埠 \_ 初始化**</dt></span><span class="sxs-lookup"><span data-stu-id="6e0c8-131"><dt>**RAS\_PORT\_INITIALIZING**</dt></span></span> </dl>           | <span data-ttu-id="6e0c8-132">連接到埠的裝置正在初始化。</span><span class="sxs-lookup"><span data-stu-id="6e0c8-132">The device attached to the port is being initialized.</span></span> <span data-ttu-id="6e0c8-133">當初始化完成時，埠的狀態將會變更為 RAS \_ 埠 \_ 接聽。</span><span class="sxs-lookup"><span data-stu-id="6e0c8-133">The state of the port will change to RAS\_PORT\_LISTENING when the initialization has been completed.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6e0c8-134">**HardwareCondition**</span><span class="sxs-lookup"><span data-stu-id="6e0c8-134">**HardwareCondition**</span></span>
</dt> <dd>

<span data-ttu-id="6e0c8-135">指定下列其中一個值，表示連接到埠的裝置狀態。</span><span class="sxs-lookup"><span data-stu-id="6e0c8-135">Specifies one of the following values to indicate the state of the device attached to the port.</span></span>



| <span data-ttu-id="6e0c8-136">值</span><span class="sxs-lookup"><span data-stu-id="6e0c8-136">Value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="6e0c8-137">意義</span><span class="sxs-lookup"><span data-stu-id="6e0c8-137">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="RAS_MODEM_OPERATIONAL"></span><span id="ras_modem_operational"></span><dl> <span data-ttu-id="6e0c8-138"><dt>**RAS \_ 數據機 \_ 操作**</dt></span><span class="sxs-lookup"><span data-stu-id="6e0c8-138"><dt>**RAS\_MODEM\_OPERATIONAL**</dt></span></span> </dl>                 | <span data-ttu-id="6e0c8-139">連接至此埠的數據機可正常運作，並已準備好接收用戶端呼叫。</span><span class="sxs-lookup"><span data-stu-id="6e0c8-139">The modem attached to this port is operational and is ready to receive client calls.</span></span><br/> |
| <span id="RAS_MODEM_HARDWARE_FAILURE"></span><span id="ras_modem_hardware_failure"></span><dl> <span data-ttu-id="6e0c8-140"><dt>**RAS \_ 數據機 \_ 硬體 \_ 故障**</dt></span><span class="sxs-lookup"><span data-stu-id="6e0c8-140"><dt>**RAS\_MODEM\_HARDWARE\_FAILURE**</dt></span></span> </dl> | <span data-ttu-id="6e0c8-141">連接至此埠的數據機有硬體問題。</span><span class="sxs-lookup"><span data-stu-id="6e0c8-141">The modem attached to this port has a hardware problem.</span></span><br/>                              |



 

</dd> <dt>

<span data-ttu-id="6e0c8-142">**LineSpeed**</span><span class="sxs-lookup"><span data-stu-id="6e0c8-142">**LineSpeed**</span></span>
</dt> <dd>

<span data-ttu-id="6e0c8-143">指定電腦可以與埠通訊的速度（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="6e0c8-143">Specifies the speed, in bits per second, with which the computer can communicate with the port.</span></span>

</dd> <dt>

<span data-ttu-id="6e0c8-144">**NumStatistics**</span><span class="sxs-lookup"><span data-stu-id="6e0c8-144">**NumStatistics**</span></span>
</dt> <dd>

<span data-ttu-id="6e0c8-145">未使用這個成員。</span><span class="sxs-lookup"><span data-stu-id="6e0c8-145">This member is not used.</span></span> <span data-ttu-id="6e0c8-146">RAS 管理功能（例如 [**RasAdminPortGetInfo**](rasadminportgetinfo.md) 函式）使用 [**ras \_ 埠 \_ 統計**](ras-port-statistics-str.md) 結構來傳回埠統計資料。</span><span class="sxs-lookup"><span data-stu-id="6e0c8-146">The RAS administration functions, such as the [**RasAdminPortGetInfo**](rasadminportgetinfo.md) function, use the [**RAS\_PORT\_STATISTICS**](ras-port-statistics-str.md) structure to return port statistics.</span></span>

</dd> <dt>

<span data-ttu-id="6e0c8-147">**NumMediaParms**</span><span class="sxs-lookup"><span data-stu-id="6e0c8-147">**NumMediaParms**</span></span>
</dt> <dd>

<span data-ttu-id="6e0c8-148">指定此埠的媒體專用參數數目。</span><span class="sxs-lookup"><span data-stu-id="6e0c8-148">Specifies the number of media-specific parameters for this port.</span></span> <span data-ttu-id="6e0c8-149">針對序列媒體，這通常是出現在 SERIAL.INI 檔案中的值數目。</span><span class="sxs-lookup"><span data-stu-id="6e0c8-149">For serial media this is typically the number of values that appear in the SERIAL.INI file.</span></span>

</dd> <dt>

<span data-ttu-id="6e0c8-150">**SizeMediaParms**</span><span class="sxs-lookup"><span data-stu-id="6e0c8-150">**SizeMediaParms**</span></span>
</dt> <dd>

<span data-ttu-id="6e0c8-151">指定所有媒體專用參數所需的緩衝區大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="6e0c8-151">Specifies the size, in bytes, of the buffer required for all media-specific parameters.</span></span> <span data-ttu-id="6e0c8-152">[**RasAdminPortGetInfo**](rasadminportgetinfo.md)函式會傳回緩衝區，其中包含 [**RAS \_ 參數**](ras-parameters-str.md)結構的陣列，以及埠的媒體參數和值。</span><span class="sxs-lookup"><span data-stu-id="6e0c8-152">The [**RasAdminPortGetInfo**](rasadminportgetinfo.md) function returns a buffer that contains an array of [**RAS\_PARAMETERS**](ras-parameters-str.md) structures with the media parameters and values for the port.</span></span>

</dd> <dt>

<span data-ttu-id="6e0c8-153">**ProjResult**</span><span class="sxs-lookup"><span data-stu-id="6e0c8-153">**ProjResult**</span></span>
</dt> <dd>

<span data-ttu-id="6e0c8-154">[**RAS \_ ppp \_ 投射 \_ 結果**](ras-ppp-projection-result-str.md)結構，指定此埠的 PPP 投射資訊。</span><span class="sxs-lookup"><span data-stu-id="6e0c8-154">A [**RAS\_PPP\_PROJECTION\_RESULT**](ras-ppp-projection-result-str.md) structure that specifies the PPP projection information for this port.</span></span> <span data-ttu-id="6e0c8-155">當 RAS 用戶端連接到伺服器時，此結構會提供每個通訊協定的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="6e0c8-155">This structure provides information for each protocol that is negotiated when a RAS client connects to a server.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6e0c8-156">規格需求</span><span class="sxs-lookup"><span data-stu-id="6e0c8-156">Requirements</span></span>



| <span data-ttu-id="6e0c8-157">需求</span><span class="sxs-lookup"><span data-stu-id="6e0c8-157">Requirement</span></span> | <span data-ttu-id="6e0c8-158">值</span><span class="sxs-lookup"><span data-stu-id="6e0c8-158">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6e0c8-159">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6e0c8-159">Minimum supported client</span></span><br/> | <span data-ttu-id="6e0c8-160">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6e0c8-160">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="6e0c8-161">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6e0c8-161">Minimum supported server</span></span><br/> | <span data-ttu-id="6e0c8-162">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6e0c8-162">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="6e0c8-163">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="6e0c8-163">End of client support</span></span><br/>    | <span data-ttu-id="6e0c8-164">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6e0c8-164">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="6e0c8-165">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="6e0c8-165">End of server support</span></span><br/>    | <span data-ttu-id="6e0c8-166">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6e0c8-166">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="6e0c8-167">標頭</span><span class="sxs-lookup"><span data-stu-id="6e0c8-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e0c8-168"><dt>Rassapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="6e0c8-168"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e0c8-169">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6e0c8-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e0c8-170">遠端存取服務 (RAS) 總覽</span><span class="sxs-lookup"><span data-stu-id="6e0c8-170">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="6e0c8-171">RAS 伺服器管理結構</span><span class="sxs-lookup"><span data-stu-id="6e0c8-171">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="6e0c8-172">**RAS \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="6e0c8-172">**RAS\_PARAMETERS**</span></span>](ras-parameters-str.md)
</dt> <dt>

[<span data-ttu-id="6e0c8-173">**RAS \_ 埠 \_ 0**</span><span class="sxs-lookup"><span data-stu-id="6e0c8-173">**RAS\_PORT\_0**</span></span>](ras-port-0-str.md)
</dt> <dt>

[<span data-ttu-id="6e0c8-174">**RAS \_ 埠 \_ 統計資料**</span><span class="sxs-lookup"><span data-stu-id="6e0c8-174">**RAS\_PORT\_STATISTICS**</span></span>](ras-port-statistics-str.md)
</dt> <dt>

[<span data-ttu-id="6e0c8-175">**RAS \_ PPP \_ 投射 \_ 結果**</span><span class="sxs-lookup"><span data-stu-id="6e0c8-175">**RAS\_PPP\_PROJECTION\_RESULT**</span></span>](ras-ppp-projection-result-str.md)
</dt> <dt>

[<span data-ttu-id="6e0c8-176">**RasAdminAcceptNewConnection**</span><span class="sxs-lookup"><span data-stu-id="6e0c8-176">**RasAdminAcceptNewConnection**</span></span>](rasadminacceptnewconnection.md)
</dt> <dt>

[<span data-ttu-id="6e0c8-177">**RasAdminConnectionHangupNotification**</span><span class="sxs-lookup"><span data-stu-id="6e0c8-177">**RasAdminConnectionHangupNotification**</span></span>](rasadminconnectionhangupnotification.md)
</dt> <dt>

[<span data-ttu-id="6e0c8-178">**RasAdminPortGetInfo**</span><span class="sxs-lookup"><span data-stu-id="6e0c8-178">**RasAdminPortGetInfo**</span></span>](rasadminportgetinfo.md)
</dt> </dl>

 

 





