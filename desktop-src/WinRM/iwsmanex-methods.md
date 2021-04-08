---
title: IWSManEx 方法
description: IWSManEx 介面會公開下列方法。
ms.assetid: 609F5D75-879A-4681-B746-8C7A8757F062
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa7279d15d98b3e534e57a83813cd9cbe75a09fc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020730"
---
# <a name="iwsmanex-methods"></a><span data-ttu-id="4058a-103">IWSManEx 方法</span><span class="sxs-lookup"><span data-stu-id="4058a-103">IWSManEx Methods</span></span>

<span data-ttu-id="4058a-104">[**IWSManEx**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex)介面會公開下列方法。</span><span class="sxs-lookup"><span data-stu-id="4058a-104">The [**IWSManEx**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex) interface exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="4058a-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="4058a-105">In this section</span></span>

-   [<span data-ttu-id="4058a-106">**CreateResourceLocator 方法**</span><span class="sxs-lookup"><span data-stu-id="4058a-106">**CreateResourceLocator Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-createresourcelocator)
-   [<span data-ttu-id="4058a-107">**EnumerationFlagHierarchyDeep 方法**</span><span class="sxs-lookup"><span data-stu-id="4058a-107">**EnumerationFlagHierarchyDeep Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchydeep)
-   [<span data-ttu-id="4058a-108">**EnumerationFlagHierarchyDeepBasePropsOnly 方法**</span><span class="sxs-lookup"><span data-stu-id="4058a-108">**EnumerationFlagHierarchyDeepBasePropsOnly Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchydeepbasepropsonly)
-   [<span data-ttu-id="4058a-109">**EnumerationFlagHierarchyShallow 方法**</span><span class="sxs-lookup"><span data-stu-id="4058a-109">**EnumerationFlagHierarchyShallow Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchyshallow)
-   [<span data-ttu-id="4058a-110">**EnumerationFlagNonXmlText 方法**</span><span class="sxs-lookup"><span data-stu-id="4058a-110">**EnumerationFlagNonXmlText Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagnonxmltext)
-   [<span data-ttu-id="4058a-111">**EnumerationFlagReturnEPR 方法**</span><span class="sxs-lookup"><span data-stu-id="4058a-111">**EnumerationFlagReturnEPR Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnepr)
-   [<span data-ttu-id="4058a-112">**EnumerationFlagReturnObject 方法**</span><span class="sxs-lookup"><span data-stu-id="4058a-112">**EnumerationFlagReturnObject Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnobject)
-   [<span data-ttu-id="4058a-113">**EnumerationFlagReturnObjectAndEPR 方法**</span><span class="sxs-lookup"><span data-stu-id="4058a-113">**EnumerationFlagReturnObjectAndEPR Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnobjectandepr)
-   [<span data-ttu-id="4058a-114">**GetErrorMessage 方法**</span><span class="sxs-lookup"><span data-stu-id="4058a-114">**GetErrorMessage Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-geterrormessage)
-   [<span data-ttu-id="4058a-115">**SessionFlagCredUsernamePassword 方法**</span><span class="sxs-lookup"><span data-stu-id="4058a-115">**SessionFlagCredUsernamePassword Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagcredusernamepassword)
-   [<span data-ttu-id="4058a-116">**SessionFlagEnableSPNServerPort 方法**</span><span class="sxs-lookup"><span data-stu-id="4058a-116">**SessionFlagEnableSPNServerPort Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagenablespnserverport)
-   [<span data-ttu-id="4058a-117">**SessionFlagNoEncryption 方法**</span><span class="sxs-lookup"><span data-stu-id="4058a-117">**SessionFlagNoEncryption Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagnoencryption)
-   [<span data-ttu-id="4058a-118">**SessionFlagSkipCACheck 方法**</span><span class="sxs-lookup"><span data-stu-id="4058a-118">**SessionFlagSkipCACheck Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagskipcacheck)
-   [<span data-ttu-id="4058a-119">**SessionFlagSkipCNCheck 方法**</span><span class="sxs-lookup"><span data-stu-id="4058a-119">**SessionFlagSkipCNCheck Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagskipcncheck)
-   [<span data-ttu-id="4058a-120">**SessionFlagUseBasic 方法**</span><span class="sxs-lookup"><span data-stu-id="4058a-120">**SessionFlagUseBasic Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusebasic)
-   [<span data-ttu-id="4058a-121">**SessionFlagUseDigest 方法**</span><span class="sxs-lookup"><span data-stu-id="4058a-121">**SessionFlagUseDigest Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusedigest)
-   [<span data-ttu-id="4058a-122">**SessionFlagUseKerberos 方法**</span><span class="sxs-lookup"><span data-stu-id="4058a-122">**SessionFlagUseKerberos Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusekerberos)
-   [<span data-ttu-id="4058a-123">**SessionFlagUseNegotiate 方法**</span><span class="sxs-lookup"><span data-stu-id="4058a-123">**SessionFlagUseNegotiate Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusenegotiate)
-   [<span data-ttu-id="4058a-124">**SessionFlagUseNoAuthentication 方法**</span><span class="sxs-lookup"><span data-stu-id="4058a-124">**SessionFlagUseNoAuthentication Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusenoauthentication)
-   [<span data-ttu-id="4058a-125">**SessionFlagUTF8 方法**</span><span class="sxs-lookup"><span data-stu-id="4058a-125">**SessionFlagUTF8 Method**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagutf8)

 

 




