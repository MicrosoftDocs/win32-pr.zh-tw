---
description: Windows 資訊安全中心
ms.assetid: FF0D7B81-AFDC-4DB2-B2B0-0D2536B2757B
title: Windows 資訊安全中心
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 694185b0a0fed7af9c2ab3d7965674c02354c079
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110073"
---
# <a name="windows-security-center"></a><span data-ttu-id="9e961-103">Windows 資訊安全中心</span><span class="sxs-lookup"><span data-stu-id="9e961-103">Windows Security Center</span></span>

<span data-ttu-id="9e961-104">Windows 安全性 Center (WSC) 是全方位的報告工具，可協助使用者建立和維護其電腦系統的保護安全層。</span><span class="sxs-lookup"><span data-stu-id="9e961-104">Windows Security Center (WSC) is a comprehensive reporting tool that helps users establish and maintain a protective security layer around their computer systems.</span></span> <span data-ttu-id="9e961-105">一旦建立安全層之後，Windows 安全性中心會 inconspicuous 監視電腦的健全狀況狀態。</span><span class="sxs-lookup"><span data-stu-id="9e961-105">Once a security layer is established, Windows Security Center is inconspicuous as it monitors the computer’s health state.</span></span> <span data-ttu-id="9e961-106">但是，如果有弱點存在，WSC 會提供警示和規範性指導方針，以協助使用者完成透過「動作中心」向終端使用者呈現的安全狀態。</span><span class="sxs-lookup"><span data-stu-id="9e961-106">However, if vulnerabilities exist, WSC provides alerts and prescriptive guidance to assist the user in achieving a secure state which is surfaced to the end user through the Action Center.</span></span>

<span data-ttu-id="9e961-107">為了讓協力廠商安全性解決方案 (防毒軟體、反惡意程式碼或反間諜功能) 符合 Windows 的規範，並且成功地將狀態回報給「動作中心」，他們必須向「安全性中心」註冊自己，並使用私人 Api 來報告任何後續狀態變更，以與 WSC 通訊。</span><span class="sxs-lookup"><span data-stu-id="9e961-107">In order for third party security solutions (antivirus, antimalware, or antispyware) to be compliant with Windows and successfully report status to Action Center, they are required to register themselves with Security Center and report any subsequent status changes using private APIs for communicating with WSC.</span></span> <span data-ttu-id="9e961-108">接著，WSC 會將這些更新傳達給「動作中心」，最後向使用者顯示這些更新。</span><span class="sxs-lookup"><span data-stu-id="9e961-108">WSC, in turn, communicates these updates to Action Center, where they are finally displayed to the end user.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9e961-109">本節內容</span><span class="sxs-lookup"><span data-stu-id="9e961-109">In this section</span></span>

-   [<span data-ttu-id="9e961-110">Windows 安全性中心列舉</span><span class="sxs-lookup"><span data-stu-id="9e961-110">Windows Security Center Enumerations</span></span>](windows-security-center-enumerations.md)
-   [<span data-ttu-id="9e961-111">Windows 安全性中心介面</span><span class="sxs-lookup"><span data-stu-id="9e961-111">Windows Security Center Interfaces</span></span>](windows-security-center-interfaces.md)
-   [<span data-ttu-id="9e961-112">Windows 安全性中心函數</span><span class="sxs-lookup"><span data-stu-id="9e961-112">Windows Security Center Functions</span></span>](windows-security-center-functions.md)

 

 



