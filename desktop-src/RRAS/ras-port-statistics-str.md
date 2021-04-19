---
title: 'RAS_PORT_STATISTICS 結構 (Rassapi .h) '
description: RAS \_ 埠 \_ 統計結構會報告 ras 伺服器為連線埠收集的統計資料。
ms.assetid: c42c7059-ff92-4f49-a86e-2f47a083aa8e
keywords:
- RAS_PORT_STATISTICS 結構 RAS
- PRAS_PORT_STATISTICS 結構指標 RAS
topic_type:
- apiref
api_name:
- RAS_PORT_STATISTICS
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85e60fb001da3f8401e47c366eecc86aced22b77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966318"
---
# <a name="ras_port_statistics-structure"></a><span data-ttu-id="1606f-105">RAS \_ 埠 \_ 統計資料結構</span><span class="sxs-lookup"><span data-stu-id="1606f-105">RAS\_PORT\_STATISTICS structure</span></span>

<span data-ttu-id="1606f-106">\[Windows Vista 不支援 **RAS \_ 埠 \_ 統計** 結構。\]</span><span class="sxs-lookup"><span data-stu-id="1606f-106">\[The **RAS\_PORT\_STATISTICS** structure is not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="1606f-107">**Ras \_ 埠 \_ 統計** 結構會報告 ras 伺服器為連線埠收集的統計資料。</span><span class="sxs-lookup"><span data-stu-id="1606f-107">The **RAS\_PORT\_STATISTICS** structure reports the statistics that a RAS server collects for a connected port.</span></span> <span data-ttu-id="1606f-108">RAS 伺服器會在每次連線埠時重設各種統計資料計數器。</span><span class="sxs-lookup"><span data-stu-id="1606f-108">The RAS server resets the various statistic counters each time the port is connected.</span></span> <span data-ttu-id="1606f-109">呼叫 [**RasAdminPortClearStatistics**](rasadminportclearstatistics.md) 函數，以強制 RAS 伺服器重設統計資料計數器。</span><span class="sxs-lookup"><span data-stu-id="1606f-109">Call the [**RasAdminPortClearStatistics**](rasadminportclearstatistics.md) function to force the RAS server to reset the statistic counters.</span></span>

<span data-ttu-id="1606f-110">針對屬於多重連結連接的埠，此結構提供兩組統計資料。</span><span class="sxs-lookup"><span data-stu-id="1606f-110">For a port that is part of a multilink connection, this structure provides two sets of statistics.</span></span> <span data-ttu-id="1606f-111">第一個集合包含連接中所有埠的累計統計資料。</span><span class="sxs-lookup"><span data-stu-id="1606f-111">The first set contains the cumulative statistics for all ports in the connection.</span></span> <span data-ttu-id="1606f-112">連接中的所有埠都有相同的統計資料。</span><span class="sxs-lookup"><span data-stu-id="1606f-112">These statistics are the same for all ports in the connection.</span></span> <span data-ttu-id="1606f-113">第二個集合只包含此埠的統計資料。</span><span class="sxs-lookup"><span data-stu-id="1606f-113">The second set contains the statistics for just this port.</span></span> <span data-ttu-id="1606f-114">如果埠不是多重連結連接的一部分，則這兩組統計資料都有相同的資訊。</span><span class="sxs-lookup"><span data-stu-id="1606f-114">If the port is not part of a multilink connection, both sets of statistics have the same information.</span></span> <span data-ttu-id="1606f-115">若要判斷埠是否為多重連結連線的一部分，請檢查埠 \_ 的 [**RAS \_ 埠 \_ 0**](ras-port-0-str.md)結構 **旗標** 成員中的埠多連結位。</span><span class="sxs-lookup"><span data-stu-id="1606f-115">To determine whether a port is part of a multilink connection, check the PORT\_MULTILINKED bit in the **Flags** member of the port's [**RAS\_PORT\_0**](ras-port-0-str.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="1606f-116">語法</span><span class="sxs-lookup"><span data-stu-id="1606f-116">Syntax</span></span>


```C++
typedef struct _RAS_PORT_STATISTICS {
  DWORD dwBytesXmited;
  DWORD dwBytesRcved;
  DWORD dwFramesXmited;
  DWORD dwFramesRcved;
  DWORD dwCrcErr;
  DWORD dwTimeoutErr;
  DWORD dwAlignmentErr;
  DWORD dwHardwareOverrunErr;
  DWORD dwFramingErr;
  DWORD dwBufferOverrunErr;
  DWORD dwBytesXmitedUncompressed;
  DWORD dwBytesRcvedUncompressed;
  DWORD dwBytesXmitedCompressed;
  DWORD dwBytesRcvedCompressed;
  DWORD dwPortBytesXmited;
  DWORD dwPortBytesRcved;
  DWORD dwPortFramesXmited;
  DWORD dwPortFramesRcved;
  DWORD dwPortCrcErr;
  DWORD dwPortTimeoutErr;
  DWORD dwPortAlignmentErr;
  DWORD dwPortHardwareOverrunErr;
  DWORD dwPortFramingErr;
  DWORD dwPortBufferOverrunErr;
  DWORD dwPortBytesXmitedUncompressed;
  DWORD dwPortBytesRcvedUncompressed;
  DWORD dwPortBytesXmitedCompressed;
  DWORD dwPortBytesRcvedCompressed;
} RAS_PORT_STATISTICS, *PRAS_PORT_STATISTICS;
```



## <a name="members"></a><span data-ttu-id="1606f-117">成員</span><span class="sxs-lookup"><span data-stu-id="1606f-117">Members</span></span>

<dl> <dt>

<span data-ttu-id="1606f-118">**dwBytesXmited**</span><span class="sxs-lookup"><span data-stu-id="1606f-118">**dwBytesXmited**</span></span>
</dt> <dd>

<span data-ttu-id="1606f-119">指定連接所傳送的位元組總數。</span><span class="sxs-lookup"><span data-stu-id="1606f-119">Specifies the total number of bytes transmitted by the connection.</span></span>

</dd> <dt>

<span data-ttu-id="1606f-120">**dwBytesRcved**</span><span class="sxs-lookup"><span data-stu-id="1606f-120">**dwBytesRcved**</span></span>
</dt> <dd>

<span data-ttu-id="1606f-121">指定連接接收的位元組總數。</span><span class="sxs-lookup"><span data-stu-id="1606f-121">Specifies the total number of bytes received by the connection.</span></span>

</dd> <dt>

<span data-ttu-id="1606f-122">**dwFramesXmited**</span><span class="sxs-lookup"><span data-stu-id="1606f-122">**dwFramesXmited**</span></span>
</dt> <dd>

<span data-ttu-id="1606f-123">指定連接所傳輸的總畫面數。</span><span class="sxs-lookup"><span data-stu-id="1606f-123">Specifies the total number of frames transmitted by the connection.</span></span>

</dd> <dt>

<span data-ttu-id="1606f-124">**dwFramesRcved**</span><span class="sxs-lookup"><span data-stu-id="1606f-124">**dwFramesRcved**</span></span>
</dt> <dd>

<span data-ttu-id="1606f-125">指定連接接收的總畫面數。</span><span class="sxs-lookup"><span data-stu-id="1606f-125">Specifies the total number of frames received by the connection.</span></span>

</dd> <dt>

<span data-ttu-id="1606f-126">**dwCrcErr**</span><span class="sxs-lookup"><span data-stu-id="1606f-126">**dwCrcErr**</span></span>
</dt> <dd>

<span data-ttu-id="1606f-127">指定連接上的 CRC 錯誤總數。</span><span class="sxs-lookup"><span data-stu-id="1606f-127">Specifies the total number of CRC errors on the connection.</span></span> <span data-ttu-id="1606f-128">CRC 錯誤是因為迴圈冗余檢查失敗所造成。</span><span class="sxs-lookup"><span data-stu-id="1606f-128">CRC errors are caused by the failure of a cyclic redundancy check.</span></span> <span data-ttu-id="1606f-129">CRC 錯誤表示收到的資料封包中有一或多個字元在抵達時發現混淆。</span><span class="sxs-lookup"><span data-stu-id="1606f-129">A CRC error indicates that one or more characters in the data packet received were found garbled on arrival.</span></span>

</dd> <dt>

<span data-ttu-id="1606f-130">**dwTimeoutErr**</span><span class="sxs-lookup"><span data-stu-id="1606f-130">**dwTimeoutErr**</span></span>
</dt> <dd>

<span data-ttu-id="1606f-131">指定連接上的逾時錯誤總數。</span><span class="sxs-lookup"><span data-stu-id="1606f-131">Specifies the total number of time-out errors on the connection.</span></span> <span data-ttu-id="1606f-132">未及時收到預期的字元時，就會發生逾時錯誤。</span><span class="sxs-lookup"><span data-stu-id="1606f-132">Time-out errors occur when an expected character is not received in time.</span></span> <span data-ttu-id="1606f-133">發生這種情況時，軟體會假設資料已遺失，並要求重新傳送。</span><span class="sxs-lookup"><span data-stu-id="1606f-133">When this occurs, the software assumes that the data has been lost and requests that it be resent.</span></span>

</dd> <dt>

<span data-ttu-id="1606f-134">**dwAlignmentErr**</span><span class="sxs-lookup"><span data-stu-id="1606f-134">**dwAlignmentErr**</span></span>
</dt> <dd>

<span data-ttu-id="1606f-135">指定連接上的對齊錯誤總數。</span><span class="sxs-lookup"><span data-stu-id="1606f-135">Specifies the total number of alignment errors on the connection.</span></span> <span data-ttu-id="1606f-136">當收到的字元不是預期的字元時，就會發生對齊錯誤。</span><span class="sxs-lookup"><span data-stu-id="1606f-136">Alignment errors occur when a character received is not the one expected.</span></span> <span data-ttu-id="1606f-137">這通常發生于遺失字元或發生逾時錯誤時。</span><span class="sxs-lookup"><span data-stu-id="1606f-137">This usually happens when a character is lost or when a time-out error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="1606f-138">**dwHardwareOverrunErr**</span><span class="sxs-lookup"><span data-stu-id="1606f-138">**dwHardwareOverrunErr**</span></span>
</dt> <dd>

<span data-ttu-id="1606f-139">指定連接上的硬體溢出錯誤總數。</span><span class="sxs-lookup"><span data-stu-id="1606f-139">Specifies the total number of hardware overrun errors on the connection.</span></span> <span data-ttu-id="1606f-140">這些錯誤指出傳送的電腦傳輸字元的速度，比接收的電腦硬體可以處理更快的次數。</span><span class="sxs-lookup"><span data-stu-id="1606f-140">These errors indicate the number of times the sending computer has transmitted characters faster than the receiving computer hardware can process them.</span></span> <span data-ttu-id="1606f-141">如果此問題持續發生，請降低用戶端的 BPS 連線速度。</span><span class="sxs-lookup"><span data-stu-id="1606f-141">If this problem persists, reduce the BPS connection rate on the client.</span></span>

</dd> <dt>

<span data-ttu-id="1606f-142">**dwFramingErr**</span><span class="sxs-lookup"><span data-stu-id="1606f-142">**dwFramingErr**</span></span>
</dt> <dd>

<span data-ttu-id="1606f-143">指定連接上的框架錯誤總數。</span><span class="sxs-lookup"><span data-stu-id="1606f-143">Specifies the total number of framing errors on the connection.</span></span> <span data-ttu-id="1606f-144">收到具有無效開始或停止位的非同步字元時，就會發生框架錯誤。</span><span class="sxs-lookup"><span data-stu-id="1606f-144">A framing error occurs when an asynchronous character is received with an invalid start or stop bit.</span></span>

</dd> <dt>

<span data-ttu-id="1606f-145">**dwBufferOverrunErr**</span><span class="sxs-lookup"><span data-stu-id="1606f-145">**dwBufferOverrunErr**</span></span>
</dt> <dd>

<span data-ttu-id="1606f-146">指定連接上的緩衝區溢位錯誤總數。</span><span class="sxs-lookup"><span data-stu-id="1606f-146">Specifies the total number of buffer overrun errors on the connection.</span></span> <span data-ttu-id="1606f-147">當傳送的電腦傳輸字元的速度比接收電腦可以容納這些字元時，就會發生緩衝區溢位錯誤。</span><span class="sxs-lookup"><span data-stu-id="1606f-147">A buffer overrun error occurs when the sending computer is transmitting characters faster than the receiving computer can accommodate them.</span></span> <span data-ttu-id="1606f-148">如果此問題持續發生，請降低用戶端的 BPS 連線速度。</span><span class="sxs-lookup"><span data-stu-id="1606f-148">If this problem persists, reduce the BPS connection rate on the client.</span></span>

</dd> <dt>

<span data-ttu-id="1606f-149">**dwBytesXmitedUncompressed**</span><span class="sxs-lookup"><span data-stu-id="1606f-149">**dwBytesXmitedUncompressed**</span></span>
</dt> <dd>

<span data-ttu-id="1606f-150">指定連接未壓縮的位元組總數。</span><span class="sxs-lookup"><span data-stu-id="1606f-150">Specifies the total number of bytes transmitted uncompressed by the connection.</span></span>

</dd> <dt>

<span data-ttu-id="1606f-151">**dwBytesRcvedUncompressed**</span><span class="sxs-lookup"><span data-stu-id="1606f-151">**dwBytesRcvedUncompressed**</span></span>
</dt> <dd>

<span data-ttu-id="1606f-152">指定連接所接收的未壓縮位元組總數。</span><span class="sxs-lookup"><span data-stu-id="1606f-152">Specifies the total number of bytes received uncompressed by the connection.</span></span>

</dd> <dt>

<span data-ttu-id="1606f-153">**dwBytesXmitedCompressed**</span><span class="sxs-lookup"><span data-stu-id="1606f-153">**dwBytesXmitedCompressed**</span></span>
</dt> <dd>

<span data-ttu-id="1606f-154">指定連接壓縮的總位元組數。</span><span class="sxs-lookup"><span data-stu-id="1606f-154">Specifies the total number of bytes transmitted compressed by the connection.</span></span>

</dd> <dt>

<span data-ttu-id="1606f-155">**dwBytesRcvedCompressed**</span><span class="sxs-lookup"><span data-stu-id="1606f-155">**dwBytesRcvedCompressed**</span></span>
</dt> <dd>

<span data-ttu-id="1606f-156">指定連接已壓縮的位元組總數。</span><span class="sxs-lookup"><span data-stu-id="1606f-156">Specifies the total number of bytes received compressed by the connection.</span></span>

</dd> <dt>

<span data-ttu-id="1606f-157">**dwPortBytesXmited**</span><span class="sxs-lookup"><span data-stu-id="1606f-157">**dwPortBytesXmited**</span></span>
</dt> <dd>

<span data-ttu-id="1606f-158">指定埠傳送的位元組總數。</span><span class="sxs-lookup"><span data-stu-id="1606f-158">Specifies the total number of bytes transmitted by the port.</span></span>

</dd> <dt>

<span data-ttu-id="1606f-159">**dwPortBytesRcved**</span><span class="sxs-lookup"><span data-stu-id="1606f-159">**dwPortBytesRcved**</span></span>
</dt> <dd>

<span data-ttu-id="1606f-160">指定埠所接收的位元組總數。</span><span class="sxs-lookup"><span data-stu-id="1606f-160">Specifies the total number of bytes received by the port.</span></span>

</dd> <dt>

<span data-ttu-id="1606f-161">**dwPortFramesXmited**</span><span class="sxs-lookup"><span data-stu-id="1606f-161">**dwPortFramesXmited**</span></span>
</dt> <dd>

<span data-ttu-id="1606f-162">指定埠所傳輸的總畫面數。</span><span class="sxs-lookup"><span data-stu-id="1606f-162">Specifies the total number of frames transmitted by the port.</span></span>

</dd> <dt>

<span data-ttu-id="1606f-163">**dwPortFramesRcved**</span><span class="sxs-lookup"><span data-stu-id="1606f-163">**dwPortFramesRcved**</span></span>
</dt> <dd>

<span data-ttu-id="1606f-164">指定埠所接收的總畫面數。</span><span class="sxs-lookup"><span data-stu-id="1606f-164">Specifies the total number of frames received by the port.</span></span>

</dd> <dt>

<span data-ttu-id="1606f-165">**dwPortCrcErr**</span><span class="sxs-lookup"><span data-stu-id="1606f-165">**dwPortCrcErr**</span></span>
</dt> <dd>

<span data-ttu-id="1606f-166">指定埠上的 CRC 錯誤總數。</span><span class="sxs-lookup"><span data-stu-id="1606f-166">Specifies the total number of CRC errors on the port.</span></span> <span data-ttu-id="1606f-167">CRC 錯誤是因為迴圈冗余檢查失敗所造成。</span><span class="sxs-lookup"><span data-stu-id="1606f-167">CRC errors are caused by the failure of a cyclic redundancy check.</span></span> <span data-ttu-id="1606f-168">CRC 錯誤表示收到的資料封包中有一或多個字元在抵達時發現混淆。</span><span class="sxs-lookup"><span data-stu-id="1606f-168">A CRC error indicates that one or more characters in the data packet received were found garbled on arrival.</span></span>

</dd> <dt>

<span data-ttu-id="1606f-169">**dwPortTimeoutErr**</span><span class="sxs-lookup"><span data-stu-id="1606f-169">**dwPortTimeoutErr**</span></span>
</dt> <dd>

<span data-ttu-id="1606f-170">指定埠上的逾時錯誤總數。</span><span class="sxs-lookup"><span data-stu-id="1606f-170">Specifies the total number of time-out errors on the port.</span></span> <span data-ttu-id="1606f-171">未及時收到預期的字元時，就會發生逾時錯誤。</span><span class="sxs-lookup"><span data-stu-id="1606f-171">Time-out errors occur when an expected character is not received in time.</span></span> <span data-ttu-id="1606f-172">發生這種情況時，軟體會假設資料已遺失，並要求重新傳送。</span><span class="sxs-lookup"><span data-stu-id="1606f-172">When this occurs, the software assumes that the data has been lost and requests that it be resent.</span></span>

</dd> <dt>

<span data-ttu-id="1606f-173">**dwPortAlignmentErr**</span><span class="sxs-lookup"><span data-stu-id="1606f-173">**dwPortAlignmentErr**</span></span>
</dt> <dd>

<span data-ttu-id="1606f-174">指定埠上的對齊錯誤總數。</span><span class="sxs-lookup"><span data-stu-id="1606f-174">Specifies the total number of alignment errors on the port.</span></span> <span data-ttu-id="1606f-175">當收到的字元不是預期的字元時，就會發生對齊錯誤。</span><span class="sxs-lookup"><span data-stu-id="1606f-175">Alignment errors occur when a character received is not the one expected.</span></span> <span data-ttu-id="1606f-176">這通常發生于遺失字元或發生逾時錯誤時。</span><span class="sxs-lookup"><span data-stu-id="1606f-176">This usually happens when a character is lost or when a time-out error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="1606f-177">**dwPortHardwareOverrunErr**</span><span class="sxs-lookup"><span data-stu-id="1606f-177">**dwPortHardwareOverrunErr**</span></span>
</dt> <dd>

<span data-ttu-id="1606f-178">指定埠上的硬體溢出錯誤總數。</span><span class="sxs-lookup"><span data-stu-id="1606f-178">Specifies the total number of hardware overrun errors on the port.</span></span> <span data-ttu-id="1606f-179">這些錯誤指出傳送的電腦傳輸字元的速度，比接收的電腦硬體可以處理更快的次數。</span><span class="sxs-lookup"><span data-stu-id="1606f-179">These errors indicate the number of times the sending computer has transmitted characters faster than the receiving computer hardware can process them.</span></span> <span data-ttu-id="1606f-180">如果此問題持續發生，請降低用戶端的 BPS 連線速度。</span><span class="sxs-lookup"><span data-stu-id="1606f-180">If this problem persists, reduce the BPS connection rate on the client.</span></span>

</dd> <dt>

<span data-ttu-id="1606f-181">**dwPortFramingErr**</span><span class="sxs-lookup"><span data-stu-id="1606f-181">**dwPortFramingErr**</span></span>
</dt> <dd>

<span data-ttu-id="1606f-182">指定埠上的框架錯誤總數。</span><span class="sxs-lookup"><span data-stu-id="1606f-182">Specifies the total number of framing errors on the port.</span></span> <span data-ttu-id="1606f-183">收到具有無效開始或停止位的非同步字元時，就會發生框架錯誤。</span><span class="sxs-lookup"><span data-stu-id="1606f-183">A framing error occurs when an asynchronous character is received with an invalid start or stop bit.</span></span>

</dd> <dt>

<span data-ttu-id="1606f-184">**dwPortBufferOverrunErr**</span><span class="sxs-lookup"><span data-stu-id="1606f-184">**dwPortBufferOverrunErr**</span></span>
</dt> <dd>

<span data-ttu-id="1606f-185">指定埠上的緩衝區溢位錯誤總數。</span><span class="sxs-lookup"><span data-stu-id="1606f-185">Specifies the total number of buffer overrun errors on the port.</span></span> <span data-ttu-id="1606f-186">當傳送的電腦傳輸字元的速度比接收電腦可以容納這些字元時，就會發生緩衝區溢位錯誤。</span><span class="sxs-lookup"><span data-stu-id="1606f-186">A buffer overrun error occurs when the sending computer is transmitting characters faster than the receiving computer can accommodate them.</span></span> <span data-ttu-id="1606f-187">如果此問題持續發生，請降低用戶端的 BPS 連線速度。</span><span class="sxs-lookup"><span data-stu-id="1606f-187">If this problem persists, reduce the BPS connection rate on the client.</span></span>

</dd> <dt>

<span data-ttu-id="1606f-188">**dwPortBytesXmitedUncompressed**</span><span class="sxs-lookup"><span data-stu-id="1606f-188">**dwPortBytesXmitedUncompressed**</span></span>
</dt> <dd>

<span data-ttu-id="1606f-189">指定埠未壓縮的總位元組數。</span><span class="sxs-lookup"><span data-stu-id="1606f-189">Specifies the total number of bytes transmitted uncompressed by the port.</span></span> <span data-ttu-id="1606f-190">如果埠是多重連結連接的一部分，此成員就無效。</span><span class="sxs-lookup"><span data-stu-id="1606f-190">If the port is part of a multilink connection, this member is not valid.</span></span> <span data-ttu-id="1606f-191">請改用連接的壓縮統計資料。</span><span class="sxs-lookup"><span data-stu-id="1606f-191">Use the compression statistics for the connection instead.</span></span>

</dd> <dt>

<span data-ttu-id="1606f-192">**dwPortBytesRcvedUncompressed**</span><span class="sxs-lookup"><span data-stu-id="1606f-192">**dwPortBytesRcvedUncompressed**</span></span>
</dt> <dd>

<span data-ttu-id="1606f-193">指定埠未壓縮的總位元組數。</span><span class="sxs-lookup"><span data-stu-id="1606f-193">Specifies the total number of bytes received uncompressed by the port.</span></span> <span data-ttu-id="1606f-194">如果埠是多重連結連接的一部分，此成員就無效。</span><span class="sxs-lookup"><span data-stu-id="1606f-194">If the port is part of a multilink connection, this member is not valid.</span></span> <span data-ttu-id="1606f-195">請改用連接的壓縮統計資料。</span><span class="sxs-lookup"><span data-stu-id="1606f-195">Use the compression statistics for the connection instead.</span></span>

</dd> <dt>

<span data-ttu-id="1606f-196">**dwPortBytesXmitedCompressed**</span><span class="sxs-lookup"><span data-stu-id="1606f-196">**dwPortBytesXmitedCompressed**</span></span>
</dt> <dd>

<span data-ttu-id="1606f-197">指定埠所壓縮的總位元組數。</span><span class="sxs-lookup"><span data-stu-id="1606f-197">Specifies the total number of bytes transmitted compressed by the port.</span></span> <span data-ttu-id="1606f-198">如果埠是多重連結連接的一部分，此成員就無效。</span><span class="sxs-lookup"><span data-stu-id="1606f-198">If the port is part of a multilink connection, this member is not valid.</span></span> <span data-ttu-id="1606f-199">請改用連接的壓縮統計資料。</span><span class="sxs-lookup"><span data-stu-id="1606f-199">Use the compression statistics for the connection instead.</span></span>

</dd> <dt>

<span data-ttu-id="1606f-200">**dwPortBytesRcvedCompressed**</span><span class="sxs-lookup"><span data-stu-id="1606f-200">**dwPortBytesRcvedCompressed**</span></span>
</dt> <dd>

<span data-ttu-id="1606f-201">指定埠已壓縮的位元組總數。</span><span class="sxs-lookup"><span data-stu-id="1606f-201">Specifies the total number of bytes received compressed by the port.</span></span> <span data-ttu-id="1606f-202">如果埠是多重連結連接的一部分，此成員就無效。</span><span class="sxs-lookup"><span data-stu-id="1606f-202">If the port is part of a multilink connection, this member is not valid.</span></span> <span data-ttu-id="1606f-203">請改用連接的壓縮統計資料。</span><span class="sxs-lookup"><span data-stu-id="1606f-203">Use the compression statistics for the connection instead.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1606f-204">規格需求</span><span class="sxs-lookup"><span data-stu-id="1606f-204">Requirements</span></span>



| <span data-ttu-id="1606f-205">需求</span><span class="sxs-lookup"><span data-stu-id="1606f-205">Requirement</span></span> | <span data-ttu-id="1606f-206">值</span><span class="sxs-lookup"><span data-stu-id="1606f-206">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1606f-207">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1606f-207">Minimum supported client</span></span><br/> | <span data-ttu-id="1606f-208">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1606f-208">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="1606f-209">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1606f-209">Minimum supported server</span></span><br/> | <span data-ttu-id="1606f-210">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1606f-210">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="1606f-211">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="1606f-211">End of client support</span></span><br/>    | <span data-ttu-id="1606f-212">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1606f-212">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="1606f-213">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="1606f-213">End of server support</span></span><br/>    | <span data-ttu-id="1606f-214">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1606f-214">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="1606f-215">標頭</span><span class="sxs-lookup"><span data-stu-id="1606f-215">Header</span></span><br/>                   | <dl> <span data-ttu-id="1606f-216"><dt>Rassapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="1606f-216"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1606f-217">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1606f-217">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1606f-218">遠端存取服務 (RAS) 總覽</span><span class="sxs-lookup"><span data-stu-id="1606f-218">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="1606f-219">RAS 伺服器管理結構</span><span class="sxs-lookup"><span data-stu-id="1606f-219">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="1606f-220">**RAS \_ 埠 \_ 0**</span><span class="sxs-lookup"><span data-stu-id="1606f-220">**RAS\_PORT\_0**</span></span>](ras-port-0-str.md)
</dt> <dt>

[<span data-ttu-id="1606f-221">**RasAdminAcceptNewConnection**</span><span class="sxs-lookup"><span data-stu-id="1606f-221">**RasAdminAcceptNewConnection**</span></span>](rasadminacceptnewconnection.md)
</dt> <dt>

[<span data-ttu-id="1606f-222">**RasAdminConnectionHangupNotification**</span><span class="sxs-lookup"><span data-stu-id="1606f-222">**RasAdminConnectionHangupNotification**</span></span>](rasadminconnectionhangupnotification.md)
</dt> <dt>

[<span data-ttu-id="1606f-223">**RasAdminPortClearStatistics**</span><span class="sxs-lookup"><span data-stu-id="1606f-223">**RasAdminPortClearStatistics**</span></span>](rasadminportclearstatistics.md)
</dt> <dt>

[<span data-ttu-id="1606f-224">**RasAdminPortGetInfo**</span><span class="sxs-lookup"><span data-stu-id="1606f-224">**RasAdminPortGetInfo**</span></span>](rasadminportgetinfo.md)
</dt> </dl>

 

 





