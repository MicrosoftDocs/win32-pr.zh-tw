---
description: 顯示用來選取憑證的對話方塊，並傳回選取的憑證集合。
ms.assetid: dbf49a4b-6da1-4819-afcd-46db89a00fce
title: ICertificates2：： Select 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Select
- ICertificates2.Select
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: cfd5b1cb5e269c14e05de25262fda711549bf02d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997800"
---
# <a name="icertificates2select-method"></a><span data-ttu-id="f3395-103">ICertificates2：： Select 方法</span><span class="sxs-lookup"><span data-stu-id="f3395-103">ICertificates2::Select method</span></span>

<span data-ttu-id="f3395-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="f3395-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="f3395-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2Collection 類別**](/previous-versions/windows/embedded/hh424013(v=msdn.10))。\]</span><span class="sxs-lookup"><span data-stu-id="f3395-105">Instead, use the [**X509Certificate2Collection Class**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="f3395-106">**Select** 方法會顯示一個對話方塊來選取憑證，並傳回選取的憑證集合。</span><span class="sxs-lookup"><span data-stu-id="f3395-106">The **Select** method displays a dialog box for selecting certificates and returns a collection of those certificates selected.</span></span> <span data-ttu-id="f3395-107">此方法是在 CAPICOM 2.0 中引進。</span><span class="sxs-lookup"><span data-stu-id="f3395-107">This method was introduced in CAPICOM 2.0.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3395-108">語法</span><span class="sxs-lookup"><span data-stu-id="f3395-108">Syntax</span></span>


```VB
Certificates.Select( _
  [ ByVal Title ], _
  [ ByVal DisplayString ], _
  [ ByVal bMultiSelect ] _
)
```



## <a name="parameters"></a><span data-ttu-id="f3395-109">參數</span><span class="sxs-lookup"><span data-stu-id="f3395-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3395-110">*標題* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="f3395-110">*Title* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f3395-111">字串，包含對話方塊的標題。</span><span class="sxs-lookup"><span data-stu-id="f3395-111">String that contains the title for the dialog box.</span></span> <span data-ttu-id="f3395-112">預設值為空字串 ("")。</span><span class="sxs-lookup"><span data-stu-id="f3395-112">The default value is an empty string ("").</span></span>

</dd> <dt>

<span data-ttu-id="f3395-113">*DisplayString* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="f3395-113">*DisplayString* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f3395-114">字串，包含對話方塊顯示的提示文字。</span><span class="sxs-lookup"><span data-stu-id="f3395-114">String that contains the prompt text displayed with the dialog box.</span></span> <span data-ttu-id="f3395-115">預設值為空字串 ("")。</span><span class="sxs-lookup"><span data-stu-id="f3395-115">The default value is an empty string ("").</span></span>

</dd> <dt>

<span data-ttu-id="f3395-116">*bMultiSelect* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="f3395-116">*bMultiSelect* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f3395-117">指出使用者是否可以選取多個憑證的布林值。</span><span class="sxs-lookup"><span data-stu-id="f3395-117">Boolean value that indicates whether the user can select more than one certificate.</span></span> <span data-ttu-id="f3395-118">True 表示可以使用 CTRL 或 SHIFT 鍵選取多個憑證。</span><span class="sxs-lookup"><span data-stu-id="f3395-118">True indicates multiple certificates can be selected by using the CTRL or SHIFT key.</span></span> <span data-ttu-id="f3395-119">預設值為 false。</span><span class="sxs-lookup"><span data-stu-id="f3395-119">The default value is false.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3395-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="f3395-120">Return value</span></span>

<span data-ttu-id="f3395-121">包含從對話方塊中選取之憑證的 [**憑證**](certificates.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="f3395-121">A [**Certificates**](certificates.md) object that contains the certificates selected from the dialog box.</span></span>

<span data-ttu-id="f3395-122">**CAPICOM 2.1：** 傳回的 [**憑證**](certificates.md) 物件包含進行選取之集合中的憑證參考。</span><span class="sxs-lookup"><span data-stu-id="f3395-122">**CAPICOM 2.1:** The [**Certificates**](certificates.md) object that is returned contains references to the certificates in the collection from which the selection was made.</span></span> <span data-ttu-id="f3395-123">對傳回的 **憑證** 物件中的憑證所做的任何變更，都會反映在該集合中。</span><span class="sxs-lookup"><span data-stu-id="f3395-123">Any changes made to the certificates in the returned **Certificates** object are reflected in that collection.</span></span>

<span data-ttu-id="f3395-124">**Capicom 2.0、capicom 2.0.0.1、capicom 2.0.0.2 和 capicom 2.0.0.3：** 傳回的 [**憑證**](certificates.md) 物件包含從中進行選取之集合中的憑證複本。</span><span class="sxs-lookup"><span data-stu-id="f3395-124">**CAPICOM 2.0, CAPICOM 2.0.0.1, CAPICOM 2.0.0.2, and CAPICOM 2.0.0.3:** The [**Certificates**](certificates.md) object that is returned contains copies of the certificates in the collection from which the selection was made.</span></span> <span data-ttu-id="f3395-125">對傳回的 **憑證** 物件中的憑證所做的任何變更都不會反映在該集合中。</span><span class="sxs-lookup"><span data-stu-id="f3395-125">Any changes made to the certificates in the returned **Certificates** object are not reflected in that collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3395-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="f3395-126">Requirements</span></span>



| <span data-ttu-id="f3395-127">需求</span><span class="sxs-lookup"><span data-stu-id="f3395-127">Requirement</span></span> | <span data-ttu-id="f3395-128">值</span><span class="sxs-lookup"><span data-stu-id="f3395-128">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f3395-129">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="f3395-129">End of client support</span></span><br/> | <span data-ttu-id="f3395-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f3395-130">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="f3395-131">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="f3395-131">End of server support</span></span><br/> | <span data-ttu-id="f3395-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f3395-132">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="f3395-133">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="f3395-133">Redistributable</span></span><br/>       | <span data-ttu-id="f3395-134">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="f3395-134">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="f3395-135">DLL</span><span class="sxs-lookup"><span data-stu-id="f3395-135">DLL</span></span><br/>                   | <dl> <span data-ttu-id="f3395-136"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3395-136"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
