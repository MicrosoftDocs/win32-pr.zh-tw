---
title: 組態設定
description: 您可以藉由變更登錄中的設定來修改控制點 API 和裝置主機 API 的行為。
ms.assetid: 81893cde-d28f-41ec-a6c1-159b3eb84274
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4107df31335da2f93fd4be669c8557b1f56d179e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106996551"
---
# <a name="configuration-settings"></a><span data-ttu-id="1aa81-103">組態設定</span><span class="sxs-lookup"><span data-stu-id="1aa81-103">Configuration Settings</span></span>

<span data-ttu-id="1aa81-104">您可以藉由變更登錄中的設定來修改 [控制點 API](control-point-api.md) 和 [裝置主機 API](device-host-api.md) 的行為。</span><span class="sxs-lookup"><span data-stu-id="1aa81-104">The behavior of the [Control Point API](control-point-api.md) and [Device Host API](device-host-api.md) can be modified by changing settings in the registry.</span></span>

<span data-ttu-id="1aa81-105">有七個會影響行為的登錄值：</span><span class="sxs-lookup"><span data-stu-id="1aa81-105">There are seven registry values that affect behavior:</span></span>

-   <span data-ttu-id="1aa81-106">**DownloadScope**</span><span class="sxs-lookup"><span data-stu-id="1aa81-106">**DownloadScope**</span></span>
-   <span data-ttu-id="1aa81-107">**DeviceLifeTime**</span><span class="sxs-lookup"><span data-stu-id="1aa81-107">**DeviceLifeTime**</span></span>
-   <span data-ttu-id="1aa81-108">\\**UPnP 裝置主機** \\檔案 **大小限制**</span><span class="sxs-lookup"><span data-stu-id="1aa81-108">\\**UPnP Device Host**\\**File Size Limit**</span></span>
-   <span data-ttu-id="1aa81-109">\\**Windows** \\**CurrentVersion** \\**UPnP** \\檔案 **大小限制**</span><span class="sxs-lookup"><span data-stu-id="1aa81-109">\\**Windows**\\**CurrentVersion**\\**UPnP**\\**File Size Limit**</span></span>
-   <span data-ttu-id="1aa81-110">**MaxCache**</span><span class="sxs-lookup"><span data-stu-id="1aa81-110">**MaxCache**</span></span>
-   <span data-ttu-id="1aa81-111">**Ttl**</span><span class="sxs-lookup"><span data-stu-id="1aa81-111">**TTL**</span></span>
-   <span data-ttu-id="1aa81-112">**ReceiveScope**</span><span class="sxs-lookup"><span data-stu-id="1aa81-112">**ReceiveScope**</span></span>

<span data-ttu-id="1aa81-113">有兩個登錄值（稱為檔案 **大小限制**），一個用於描述檔，另一個則用於使用簡單物件存取通訊協定 (SOAP) 的回應。</span><span class="sxs-lookup"><span data-stu-id="1aa81-113">There are two registry values called **File Size Limit**, one for description documents and the other for responses that use Simple Object Access Protocol (SOAP).</span></span>

<span data-ttu-id="1aa81-114">登錄中每個值的位置如下所示：</span><span class="sxs-lookup"><span data-stu-id="1aa81-114">The location of each of the seven values in the registry is as follows:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         UPnPControl Point
            DownloadScope
         UPnP Device Host
            Devices
               DeviceLifeTime
            File Size Limit
         Windows
            CurrentVersion
               UPnP
                  File Size Limit
   SYSTEM
      CurentControlSet
         Services
            SSDPSRV
               Parameters
                  MaxCache
                  TTL
                  ReceiveScope
```

## <a name="registry-value-descriptions"></a><span data-ttu-id="1aa81-115">登錄值描述</span><span class="sxs-lookup"><span data-stu-id="1aa81-115">Registry Value Descriptions</span></span>

<span data-ttu-id="1aa81-116">下列清單將說明登錄值。</span><span class="sxs-lookup"><span data-stu-id="1aa81-116">The registry values are explained in the following list.</span></span> <span data-ttu-id="1aa81-117">每個登錄值都是 **REG \_ DWORD** (32 位整數) 。</span><span class="sxs-lookup"><span data-stu-id="1aa81-117">Each registry value is a **REG\_DWORD** (a 32-bit integer).</span></span> <span data-ttu-id="1aa81-118">每個值的作用都是全域的。</span><span class="sxs-lookup"><span data-stu-id="1aa81-118">The effect of each value is global.</span></span>

<dl> <dt>

<span data-ttu-id="1aa81-119"><span id="DownloadScope"></span><span id="downloadscope"></span><span id="DOWNLOADSCOPE"></span>**DownloadScope**</span><span class="sxs-lookup"><span data-stu-id="1aa81-119"><span id="DownloadScope"></span><span id="downloadscope"></span><span id="DOWNLOADSCOPE"></span>**DownloadScope**</span></span>
</dt> <dd>

<span data-ttu-id="1aa81-120">指定適用于裝置描述檔 URL 的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="1aa81-120">Specifies which IP addresses are valid for the device description document URL.</span></span> <span data-ttu-id="1aa81-121">如果描述檔 URL 中所指定主機的 IP 位址不在 **DownloadScope** 指定的範圍內，則該 ip 位址無效，且不會建立裝置物件。</span><span class="sxs-lookup"><span data-stu-id="1aa81-121">If the IP address of the host that is specified in the description document URL is not within the scope specified by **DownloadScope**, that IP address is not valid and the device object will not be created.</span></span>

<span data-ttu-id="1aa81-122">有效的值如下表所示。</span><span class="sxs-lookup"><span data-stu-id="1aa81-122">The valid values are shown in the following table.</span></span> <span data-ttu-id="1aa81-123">預設值為 1。</span><span class="sxs-lookup"><span data-stu-id="1aa81-123">The default value is 1.</span></span>



| <span data-ttu-id="1aa81-124">**DownloadScope** 的值</span><span class="sxs-lookup"><span data-stu-id="1aa81-124">Value of **DownloadScope**</span></span> | <span data-ttu-id="1aa81-125">意義</span><span class="sxs-lookup"><span data-stu-id="1aa81-125">Meaning</span></span>                                                                                                                                                                                                    |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1aa81-126">0</span><span class="sxs-lookup"><span data-stu-id="1aa81-126">0</span></span>                          | <span data-ttu-id="1aa81-127">主機的 IP 位址必須是子網位址。</span><span class="sxs-lookup"><span data-stu-id="1aa81-127">Host's IP address must be a subnet address.</span></span>                                                                                                                                                                |
| <span data-ttu-id="1aa81-128">1</span><span class="sxs-lookup"><span data-stu-id="1aa81-128">1</span></span>                          | <span data-ttu-id="1aa81-129">主機的 IP 位址必須是子網位址或私用位址，也就是其中一個10。*x*。*x*。*x*、192.168。*x*。*x*、172.16。*x*。*x* (，如 RFC 1918) 或169.254 所指定。*x*。*x* (，如 RFC 3330) 所指定。</span><span class="sxs-lookup"><span data-stu-id="1aa81-129">Host's IP address must be a subnet address or a private address which is one of 10.*x*.*x*.*x*, 192.168.*x*.*x*, 172.16.*x*.*x* (as specified by RFC 1918), or 169.254.*x*.*x* (as specified by RFC 3330).</span></span> |
| <span data-ttu-id="1aa81-130">2</span><span class="sxs-lookup"><span data-stu-id="1aa81-130">2</span></span>                          | <span data-ttu-id="1aa81-131">主機的 IP 位址必須是子網位址、私人位址，或是來自控制點的存留時間 (TTL) 躍點內的位址。</span><span class="sxs-lookup"><span data-stu-id="1aa81-131">Host's IP address must be a subnet address, private address, or an address that is within the time-to-live (TTL) hops from the control point.</span></span>                                                              |
| <span data-ttu-id="1aa81-132">3</span><span class="sxs-lookup"><span data-stu-id="1aa81-132">3</span></span>                          | <span data-ttu-id="1aa81-133">主機的 IP 位址可以是任何位址。</span><span class="sxs-lookup"><span data-stu-id="1aa81-133">Host's IP address can be any address.</span></span>                                                                                                                                                                      |
| <span data-ttu-id="1aa81-134">>3</span><span class="sxs-lookup"><span data-stu-id="1aa81-134">>3</span></span>                      | <span data-ttu-id="1aa81-135">與值0相同。</span><span class="sxs-lookup"><span data-stu-id="1aa81-135">Same as that for the value 0.</span></span>                                                                                                                                                                              |



 

</dd> <dt>

<span data-ttu-id="1aa81-136"><span id="DeviceLifeTime"></span><span id="devicelifetime"></span><span id="DEVICELIFETIME"></span>**DeviceLifeTime**</span><span class="sxs-lookup"><span data-stu-id="1aa81-136"><span id="DeviceLifeTime"></span><span id="devicelifetime"></span><span id="DEVICELIFETIME"></span>**DeviceLifeTime**</span></span>
</dt> <dd>

<span data-ttu-id="1aa81-137">選擇性。</span><span class="sxs-lookup"><span data-stu-id="1aa81-137">Optional.</span></span> <span data-ttu-id="1aa81-138">指定裝置的存留期（以秒為單位），以覆寫裝置公告訊息中提供的值。</span><span class="sxs-lookup"><span data-stu-id="1aa81-138">Specifies a device's lifetime, in seconds, which overrides the value provided in the device's announcement message.</span></span> <span data-ttu-id="1aa81-139">如果有 **DeviceLifeTime** ，則會忽略裝置宣告中指定的值，而改為使用登錄值。</span><span class="sxs-lookup"><span data-stu-id="1aa81-139">If **DeviceLifeTime** is present, the value specified in the device's announcement is ignored and the registry value is used instead.</span></span> <span data-ttu-id="1aa81-140">這適用于所有裝置。</span><span class="sxs-lookup"><span data-stu-id="1aa81-140">This applies to all devices.</span></span>

<span data-ttu-id="1aa81-141">有效的值範圍從900到 **最大的 \_ DWORD**。</span><span class="sxs-lookup"><span data-stu-id="1aa81-141">Valid values range from 900 through **MAX\_DWORD**.</span></span> <span data-ttu-id="1aa81-142">預設值是 1800秒。</span><span class="sxs-lookup"><span data-stu-id="1aa81-142">The default value is 1800.</span></span> <span data-ttu-id="1aa81-143">如果 **DeviceLifeTime** 設為0，則會使用預設值。</span><span class="sxs-lookup"><span data-stu-id="1aa81-143">If **DeviceLifeTime** is set to 0, the default value is used.</span></span>

</dd> <dt>

<span data-ttu-id="1aa81-144"><span id="_UPnP_Device_HostFile_Size_Limit"></span><span id="_upnp_device_hostfile_size_limit"></span><span id="_UPNP_DEVICE_HOSTFILE_SIZE_LIMIT"></span>\\**UPnP 裝置主機** \\檔案 **大小限制**</span><span class="sxs-lookup"><span data-stu-id="1aa81-144"><span id="_UPnP_Device_HostFile_Size_Limit"></span><span id="_upnp_device_hostfile_size_limit"></span><span id="_UPNP_DEVICE_HOSTFILE_SIZE_LIMIT"></span>\\**UPnP Device Host**\\**File Size Limit**</span></span>
</dt> <dd>

<span data-ttu-id="1aa81-145">指定每個描述檔的大小上限（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="1aa81-145">Specifies the maximum size, in bytes, of each description document.</span></span> <span data-ttu-id="1aa81-146">這項設定無法在 Windows XP Service Pack 2 之前的 Windows 版本中設定。</span><span class="sxs-lookup"><span data-stu-id="1aa81-146">This setting is not configurable in versions of Windows preceding Windows XP Service Pack 2.</span></span> <span data-ttu-id="1aa81-147">在先前的版本中，此設定是硬式編碼為102400。</span><span class="sxs-lookup"><span data-stu-id="1aa81-147">In the previous versions, this setting is hard-coded as 102400.</span></span>

<span data-ttu-id="1aa81-148">有效的值範圍從10240到 **最大的 \_ DWORD**。</span><span class="sxs-lookup"><span data-stu-id="1aa81-148">Valid values range from 10240 through **MAX\_DWORD**.</span></span> <span data-ttu-id="1aa81-149">預設值為102400。</span><span class="sxs-lookup"><span data-stu-id="1aa81-149">The default value is 102400.</span></span>

</dd> <dt>

<span data-ttu-id="1aa81-150"><span id="_WindowsCurrentVersionUPnPFile_Size_Limit"></span><span id="_windowscurrentversionupnpfile_size_limit"></span><span id="_WINDOWSCURRENTVERSIONUPNPFILE_SIZE_LIMIT"></span>\\**Windows** \\**CurrentVersion** \\**UPnP** \\檔案 **大小限制**</span><span class="sxs-lookup"><span data-stu-id="1aa81-150"><span id="_WindowsCurrentVersionUPnPFile_Size_Limit"></span><span id="_windowscurrentversionupnpfile_size_limit"></span><span id="_WINDOWSCURRENTVERSIONUPNPFILE_SIZE_LIMIT"></span>\\**Windows**\\**CurrentVersion**\\**UPnP**\\**File Size Limit**</span></span>
</dt> <dd>

<span data-ttu-id="1aa81-151">指定可接受之 SOAP 回應的大小上限（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="1aa81-151">Specifies the maximum size, in bytes, of the SOAP response that is acceptable.</span></span> <span data-ttu-id="1aa81-152">這項設定無法在 Windows XP Service Pack 2 之前的 Windows 版本中設定。</span><span class="sxs-lookup"><span data-stu-id="1aa81-152">This setting is not configurable in versions of Windows preceding Windows XP Service Pack 2.</span></span> <span data-ttu-id="1aa81-153">在先前的版本中，此設定是硬式編碼為102400。</span><span class="sxs-lookup"><span data-stu-id="1aa81-153">In the previous versions, this setting is hard-coded as 102400.</span></span>

<span data-ttu-id="1aa81-154">有效的值範圍從10240到 **最大的 \_ DWORD**。</span><span class="sxs-lookup"><span data-stu-id="1aa81-154">Valid values range from 10240 through **MAX\_DWORD**.</span></span> <span data-ttu-id="1aa81-155">預設值為102400。</span><span class="sxs-lookup"><span data-stu-id="1aa81-155">The default value is 102400.</span></span>

</dd> <dt>

<span data-ttu-id="1aa81-156"><span id="MaxCache"></span><span id="maxcache"></span><span id="MAXCACHE"></span>**MaxCache**</span><span class="sxs-lookup"><span data-stu-id="1aa81-156"><span id="MaxCache"></span><span id="maxcache"></span><span id="MAXCACHE"></span>**MaxCache**</span></span>
</dt> <dd>

<span data-ttu-id="1aa81-157">指定簡易服務探索通訊協定中允許的最大專案數 (SSDP) 快取。</span><span class="sxs-lookup"><span data-stu-id="1aa81-157">Specifies the maximum number of entries allowed in the Simple Service Discovery Protocol (SSDP) cache.</span></span>

<span data-ttu-id="1aa81-158">有效的值範圍從10到30000。</span><span class="sxs-lookup"><span data-stu-id="1aa81-158">Valid values range from 10 through 30000.</span></span> <span data-ttu-id="1aa81-159">預設值為 1000。</span><span class="sxs-lookup"><span data-stu-id="1aa81-159">The default value is 1000.</span></span>

</dd> <dt>

<span data-ttu-id="1aa81-160"><span id="TTL"></span><span id="ttl"></span>**Ttl**</span><span class="sxs-lookup"><span data-stu-id="1aa81-160"><span id="TTL"></span><span id="ttl"></span>**TTL**</span></span>
</dt> <dd>

<span data-ttu-id="1aa81-161">指定 SSDP 封包的存留時間。</span><span class="sxs-lookup"><span data-stu-id="1aa81-161">Specifies the time-to-live for an SSDP packet.</span></span> <span data-ttu-id="1aa81-162">亦即， **TTL** 會指定封包允許的躍點數目。</span><span class="sxs-lookup"><span data-stu-id="1aa81-162">That is, **TTL** specifies the number of hops allowed for a packet.</span></span>

<span data-ttu-id="1aa81-163">有效的值範圍從1到255。</span><span class="sxs-lookup"><span data-stu-id="1aa81-163">Valid values range from 1 through 255.</span></span> <span data-ttu-id="1aa81-164">預設值為 1。</span><span class="sxs-lookup"><span data-stu-id="1aa81-164">The default value is 1.</span></span>

</dd> <dt>

<span data-ttu-id="1aa81-165"><span id="ReceiveScope"></span><span id="receivescope"></span><span id="RECEIVESCOPE"></span>**ReceiveScope**</span><span class="sxs-lookup"><span data-stu-id="1aa81-165"><span id="ReceiveScope"></span><span id="receivescope"></span><span id="RECEIVESCOPE"></span>**ReceiveScope**</span></span>
</dt> <dd>

<span data-ttu-id="1aa81-166">指定哪些 IP 位址是訊息的有效來源。</span><span class="sxs-lookup"><span data-stu-id="1aa81-166">Specifies which IP addresses are valid sources of a message.</span></span> <span data-ttu-id="1aa81-167">如果傳入訊息源自于 **ReceiveScope** 所指定之範圍內的位址，則會忽略該訊息。</span><span class="sxs-lookup"><span data-stu-id="1aa81-167">If an incoming message originates from an address that is not within the scope specified by **ReceiveScope**, the message is ignored.</span></span> <span data-ttu-id="1aa81-168">這項設定無法在 Windows XP Service Pack 2 之前的 Windows 版本中設定。</span><span class="sxs-lookup"><span data-stu-id="1aa81-168">This setting is not configurable in versions of Windows preceding Windows XP Service Pack 2.</span></span> <span data-ttu-id="1aa81-169">在先前的版本中，會接受訊息，而不考慮其來源。</span><span class="sxs-lookup"><span data-stu-id="1aa81-169">In the previous versions, a message is accepted without regard to its source.</span></span>

<span data-ttu-id="1aa81-170">有效的值如下表所示。</span><span class="sxs-lookup"><span data-stu-id="1aa81-170">The valid values are shown in the following table.</span></span> <span data-ttu-id="1aa81-171">預設值為 1。</span><span class="sxs-lookup"><span data-stu-id="1aa81-171">The default value is 1.</span></span>



| <span data-ttu-id="1aa81-172">**ReceiveScope** 的值</span><span class="sxs-lookup"><span data-stu-id="1aa81-172">Value of **ReceiveScope**</span></span> | <span data-ttu-id="1aa81-173">意義</span><span class="sxs-lookup"><span data-stu-id="1aa81-173">Meaning</span></span>                                                                                                                                                                                                      |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1aa81-174">0</span><span class="sxs-lookup"><span data-stu-id="1aa81-174">0</span></span>                         | <span data-ttu-id="1aa81-175">寄件者的 IP 位址必須是子網位址。</span><span class="sxs-lookup"><span data-stu-id="1aa81-175">Sender's IP address must be a subnet address.</span></span>                                                                                                                                                                |
| <span data-ttu-id="1aa81-176">1</span><span class="sxs-lookup"><span data-stu-id="1aa81-176">1</span></span>                         | <span data-ttu-id="1aa81-177">寄件者的 IP 位址必須是子網位址或私用位址，也就是其中一個10。*x*。*x*。*x*、192.168。*x*。*x*、172.16。*x*。*x* (，如 RFC 1918) 或169.254 所指定。*x*。*x* (，如 RFC 3330) 所指定。</span><span class="sxs-lookup"><span data-stu-id="1aa81-177">Sender's IP address must be a subnet address or a private address which is one of 10.*x*.*x*.*x*, 192.168.*x*.*x*, 172.16.*x*.*x* (as specified by RFC 1918), or 169.254.*x*.*x* (as specified by RFC 3330).</span></span> |
| <span data-ttu-id="1aa81-178">2</span><span class="sxs-lookup"><span data-stu-id="1aa81-178">2</span></span>                         | <span data-ttu-id="1aa81-179">未使用。</span><span class="sxs-lookup"><span data-stu-id="1aa81-179">Not used.</span></span> <span data-ttu-id="1aa81-180">如果 **ReceiveScope** 設定為2，則會使用預設值。</span><span class="sxs-lookup"><span data-stu-id="1aa81-180">If **ReceiveScope** is set to 2, the default value is used.</span></span>                                                                                                                                        |
| <span data-ttu-id="1aa81-181">3</span><span class="sxs-lookup"><span data-stu-id="1aa81-181">3</span></span>                         | <span data-ttu-id="1aa81-182">寄件者的 IP 位址可以是任何位址。</span><span class="sxs-lookup"><span data-stu-id="1aa81-182">Sender's IP address can be any address.</span></span>                                                                                                                                                                      |



 

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="1aa81-183">相關主題</span><span class="sxs-lookup"><span data-stu-id="1aa81-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1aa81-184">UPnP 架構總覽</span><span class="sxs-lookup"><span data-stu-id="1aa81-184">Overview of UPnP Architecture</span></span>](overview-of-universal-plug-and-play.md)
</dt> </dl>

 

 




