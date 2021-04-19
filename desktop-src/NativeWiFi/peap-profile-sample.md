---
description: 用來連線到使用受保護的可延伸驗證通訊協定第2版 (PEAP Eap-mschapv2) 搭配使用者名稱/密碼進行 802.1 X 驗證的網路。
ms.assetid: b5dde0d0-940f-40ec-b24d-95a76325ff1b
title: PEAP 設定檔範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db34a3a99305f3506e3b34fde48f41e5a4c72ac8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974263"
---
# <a name="peap-profile-sample"></a><span data-ttu-id="76f0a-103">PEAP 設定檔範例</span><span class="sxs-lookup"><span data-stu-id="76f0a-103">PEAP Profile Sample</span></span>

<span data-ttu-id="76f0a-104">此設定檔範例會顯示有線網路設定檔，用來連線到使用受保護的可延伸驗證通訊協定第2版 (PEAP-Eap-mschapv2) 搭配 \* UserName \* **/** _Password_ for 802.1 x Authentication 的網路。</span><span class="sxs-lookup"><span data-stu-id="76f0a-104">This profile sample shows a wired network profile used to connect to a network that uses Protected Extensible Authentication Protocol with Microsoft Challenge Handshake Authentication Protocol version 2 (PEAP-MSCHAPv2) with \*UserName\***/**_Password_ for 802.1X authentication.</span></span> <span data-ttu-id="76f0a-105">系統會提示使用者輸入認證。</span><span class="sxs-lookup"><span data-stu-id="76f0a-105">The user is prompted to enter credentials.</span></span>

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<LANProfile xmlns="https://www.microsoft.com/networking/LAN/profile/v1">
    <MSM>
        <security>
            <OneXEnforced>false</OneXEnforced>
            <OneXEnabled>true</OneXEnabled>
            <OneX xmlns="https://www.microsoft.com/networking/OneX/v1">
                <EAPConfig>
                    <EapHostConfig xmlns="https://www.microsoft.com/provisioning/EapHostConfig" 
                                   xmlns:eapCommon="https://www.microsoft.com/provisioning/EapCommon" 
                                   xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapMethodConfig">
                        <EapMethod>
                            <eapCommon:Type>25</eapCommon:Type> 
                            <eapCommon:AuthorId>0</eapCommon:AuthorId> 
                       </EapMethod>
                       <Config xmlns:baseEap="https://www.microsoft.com/provisioning/BaseEapConnectionPropertiesV1" 
                               xmlns:msPeap="https://www.microsoft.com/provisioning/MsPeapConnectionPropertiesV1" 
                               xmlns:msChapV2="https://www.microsoft.com/provisioning/MsChapV2ConnectionPropertiesV1">
                           <baseEap:Eap>
                               <baseEap:Type>25</baseEap:Type> 
                               <msPeap:EapType>
                                   <msPeap:ServerValidation>
                                       <msPeap:DisableUserPromptForServerValidation>false</msPeap:DisableUserPromptForServerValidation> 
                                       <msPeap:TrustedRootCA /> 
                                   </msPeap:ServerValidation>
                                   <msPeap:FastReconnect>true</msPeap:FastReconnect> 
                                   <msPeap:InnerEapOptional>0</msPeap:InnerEapOptional> 
                                   <baseEap:Eap>
                                       <baseEap:Type>26</baseEap:Type> 
                                       <msChapV2:EapType>
                                           <msChapV2:UseWinLogonCredentials>false</msChapV2:UseWinLogonCredentials> 
                                       </msChapV2:EapType>
                                   </baseEap:Eap>
                                   <msPeap:EnableQuarantineChecks>false</msPeap:EnableQuarantineChecks> 
                                   <msPeap:RequireCryptoBinding>false</msPeap:RequireCryptoBinding> 
                                   <msPeap:PeapExtensions /> 
                               </msPeap:EapType>
                           </baseEap:Eap>
                       </Config>
                   </EapHostConfig>
                </EAPConfig>
            </OneX>
        </security>
    </MSM>
</LANProfile>
```

## <a name="related-topics"></a><span data-ttu-id="76f0a-106">相關主題</span><span class="sxs-lookup"><span data-stu-id="76f0a-106">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76f0a-107">有線設定檔範例</span><span class="sxs-lookup"><span data-stu-id="76f0a-107">Wired Profile Samples</span></span>](wired-profile-samples.md)
</dt> </dl>

 

 



