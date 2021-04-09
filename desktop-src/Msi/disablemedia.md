---
description: 如果每個使用者的系統原則設定為 &\# 0034; 1&\# 0034; 則執行某項產品維護安裝的使用者和系統管理員，將無法使用 [流覽] 對話方塊來流覽媒體來源（如 cd-rom），以取得其他可安裝產品的來源。
ms.assetid: 275a6d43-ecf8-4146-82eb-3b42b25b9a80
title: DisableMedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2ee50abf36225aa96e52332a53f0b2ab36f058c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "103945588"
---
# <a name="disablemedia"></a><span data-ttu-id="55c3c-103">DisableMedia</span><span class="sxs-lookup"><span data-stu-id="55c3c-103">DisableMedia</span></span>

<span data-ttu-id="55c3c-104">如果每個使用者的 [系統原則](system-policy.md) 設定為 "1"，則執行某項產品之維護安裝的使用者和系統管理員，將無法使用 [流覽] 對話方塊來流覽其他可安裝產品來源的媒體來源，例如 cd-rom。</span><span class="sxs-lookup"><span data-stu-id="55c3c-104">If this per-user [system policy](system-policy.md) is set to "1", users and administrators running a maintenance installation of one product are prevented from using the Browse Dialog to browse media sources, such as CD-ROM, for the sources of other installable products.</span></span> <span data-ttu-id="55c3c-105">無論是否以較高的許可權進行安裝，都會防止流覽其他產品。</span><span class="sxs-lookup"><span data-stu-id="55c3c-105">Browsing for other products is prevented regardless of whether the installation is done with elevated privileges.</span></span> <span data-ttu-id="55c3c-106">如果使用者已正確標示媒體來源，則使用者仍然可以從媒體重新安裝產品。</span><span class="sxs-lookup"><span data-stu-id="55c3c-106">It is still possible for the user to reinstall the product from media if the user has a correctly labeled media source.</span></span>

## <a name="registry-key"></a><span data-ttu-id="55c3c-107">登錄金鑰</span><span class="sxs-lookup"><span data-stu-id="55c3c-107">Registry Key</span></span>

<span data-ttu-id="55c3c-108">**HKEY \_目前的 \_ 使用者** \\ **軟體** \\ **原則** \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="55c3c-108">**HKEY\_CURRENT\_USER**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="55c3c-109">資料類型</span><span class="sxs-lookup"><span data-stu-id="55c3c-109">Data Type</span></span>

<span data-ttu-id="55c3c-110">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="55c3c-110">**REG\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="55c3c-111">備註</span><span class="sxs-lookup"><span data-stu-id="55c3c-111">Remarks</span></span>

<span data-ttu-id="55c3c-112">請注意， [**DISABLEMEDIA**](-disablemedia.md) 屬性與 DISABLEMEDIA 原則的效果不同。</span><span class="sxs-lookup"><span data-stu-id="55c3c-112">Note that the [**DISABLEMEDIA**](-disablemedia.md) property has a different effect than the DisableMedia policy.</span></span> <span data-ttu-id="55c3c-113">設定 DisableMedia 系統原則，只會停用流覽至媒體來源。</span><span class="sxs-lookup"><span data-stu-id="55c3c-113">Setting the DisableMedia system policy, only disables browsing to media sources.</span></span> <span data-ttu-id="55c3c-114">設定 **DISABLEMEDIA** 屬性可防止安裝程式將任何媒體來源（例如 cd-rom）註冊為產品的有效來源。</span><span class="sxs-lookup"><span data-stu-id="55c3c-114">Setting the **DISABLEMEDIA** property prevents the installer from registering any media source, such as a CD-ROM, as a valid source for the product.</span></span> <span data-ttu-id="55c3c-115">但是，如果已啟用流覽，使用者仍可流覽至媒體來源。</span><span class="sxs-lookup"><span data-stu-id="55c3c-115">If browsing is enabled however, a user may still browse to a media source.</span></span>

## <a name="related-topics"></a><span data-ttu-id="55c3c-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="55c3c-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55c3c-117">來源復原</span><span class="sxs-lookup"><span data-stu-id="55c3c-117">Source Resiliency</span></span>](source-resiliency.md)
</dt> </dl>

 

 



