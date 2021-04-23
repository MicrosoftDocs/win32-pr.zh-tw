---
description: 顯示允許使用者選取憑證的對話方塊。
ms.assetid: 242c19a7-179b-4fc0-a050-a1b598566a6b
title: CryptUIDlgSelectCertificate 函式
ms.topic: reference
ms.date: 05/29/2020
ms.openlocfilehash: 8f015796671990491407d91cbd51761816c5434b
ms.sourcegitcommit: 435ea8f5bf06808ffa7dce39afb0ee6de842ba2f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/23/2021
ms.locfileid: "107925689"
---
# <a name="cryptuidlgselectcertificate-function"></a><span data-ttu-id="ebec0-103">CryptUIDlgSelectCertificate 函式</span><span class="sxs-lookup"><span data-stu-id="ebec0-103">CryptUIDlgSelectCertificate function</span></span>

<span data-ttu-id="ebec0-104">**CryptUIDlgSelectCertificate** 函式會顯示可讓使用者選取憑證的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="ebec0-104">The **CryptUIDlgSelectCertificate** function displays a dialog box that allows a user to select a certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebec0-105">語法</span><span class="sxs-lookup"><span data-stu-id="ebec0-105">Syntax</span></span>


```C++
PCCERT_CONTEXT WINAPI CryptUIDlgSelectCertificate(
  _In_  PCCRYPTUI_SELECTCERTIFICATE_STRUCT pcsc
);
```



## <a name="parameters"></a><span data-ttu-id="ebec0-106">參數</span><span class="sxs-lookup"><span data-stu-id="ebec0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebec0-107">*pcsc* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ebec0-107">*pcsc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebec0-108">[**CRYPTUI \_ SELECTCERTIFICATE \_ 結構**](cryptui-selectcertificate-struct.md)結構的指標，其中包含要顯示之對話方塊的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ebec0-108">A pointer to a [**CRYPTUI\_SELECTCERTIFICATE\_STRUCT**](cryptui-selectcertificate-struct.md) structure that contains information about the dialog box to display.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebec0-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="ebec0-109">Return value</span></span>

<span data-ttu-id="ebec0-110">憑證 [**\_ 內容**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_context) 結構的指標，表示使用者選取的憑證。</span><span class="sxs-lookup"><span data-stu-id="ebec0-110">A pointer to a [**CERT\_CONTEXT**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_context) structure that represents the certificate selected by the user.</span></span> <span data-ttu-id="ebec0-111">當您完成使用此憑證時，您必須將此指標傳遞至 [**CertFreeCertificateCoNtext**](/windows/win32/api/wincrypt/nf-wincrypt-certfreecertificatecontext) 函式，以遞減憑證內容的參考計數。</span><span class="sxs-lookup"><span data-stu-id="ebec0-111">When you have finished using this certificate, you must pass this pointer to the [**CertFreeCertificateContext**](/windows/win32/api/wincrypt/nf-wincrypt-certfreecertificatecontext) function to decrement the reference count of the certificate context.</span></span>

<span data-ttu-id="ebec0-112">如果 *pcsc* 結構的 **dwFlags** 成員未包含 **CRYPTUI \_ SELECTCERT \_ 多重** 選取旗標，則傳回值為 **Null** 表示使用者已關閉對話方塊，而不選取憑證。</span><span class="sxs-lookup"><span data-stu-id="ebec0-112">If the **dwFlags** member of the *pcsc* structure does not contain the **CRYPTUI\_SELECTCERT\_MULTISELECT** flag, a return value of **NULL** means that the user closed the dialog box without selecting a certificate.</span></span>

<span data-ttu-id="ebec0-113">如果 *pcsc* 結構的 **DwFlags** 成員包含 **CRYPTUI \_ SELECTCERT \_ 多重** 複選旗標，此函數一律會傳回 **Null**。</span><span class="sxs-lookup"><span data-stu-id="ebec0-113">If the **dwFlags** member of the *pcsc* structure does contain the **CRYPTUI\_SELECTCERT\_MULTISELECT** flag, this function always returns **NULL**.</span></span> <span data-ttu-id="ebec0-114">選取的憑證將包含在 *pcsc* 的 **hSelectedCertStore** 成員所代表的憑證存放區中。</span><span class="sxs-lookup"><span data-stu-id="ebec0-114">The selected certificates will be contained in the certificate store that is represented by the **hSelectedCertStore** member of *pcsc*.</span></span> <span data-ttu-id="ebec0-115">如果存放區中的憑證數目在呼叫 **CryptUIDlgSelectCertificate** 之前和之後是相同的，使用者會關閉對話方塊，而不選取任何憑證。</span><span class="sxs-lookup"><span data-stu-id="ebec0-115">If the number of certificates in the store is the same before and after calling **CryptUIDlgSelectCertificate**, the user closed the dialog box without selecting any certificates.</span></span>

## <a name="remarks"></a><span data-ttu-id="ebec0-116">備註</span><span class="sxs-lookup"><span data-stu-id="ebec0-116">Remarks</span></span>

<span data-ttu-id="ebec0-117">如果 [**CRYPTUI \_ SELECTCERTIFICATE \_ 結構**](cryptui-selectcertificate-struct.md)結構的 **dwFlags** 成員設定為 **CRYPTUI \_ SELECTCERT \_ 舊版**，則會顯示舊版對話方塊。</span><span class="sxs-lookup"><span data-stu-id="ebec0-117">If the **dwFlags** member of the [**CRYPTUI\_SELECTCERTIFICATE\_STRUCT**](cryptui-selectcertificate-struct.md) structure is set to **CRYPTUI\_SELECTCERT\_LEGACY**, the legacy dialog is displayed.</span></span> <span data-ttu-id="ebec0-118">否則，就會顯示目前的憑證選擇對話方塊。</span><span class="sxs-lookup"><span data-stu-id="ebec0-118">Otherwise, the current certificate selection dialog is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebec0-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="ebec0-119">Requirements</span></span>



| <span data-ttu-id="ebec0-120">需求</span><span class="sxs-lookup"><span data-stu-id="ebec0-120">Requirement</span></span> | <span data-ttu-id="ebec0-121">值</span><span class="sxs-lookup"><span data-stu-id="ebec0-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebec0-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ebec0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ebec0-123">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ebec0-123">Windows�XP \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="ebec0-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ebec0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ebec0-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ebec0-125">Windows Server�2003 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="ebec0-126">結束支援</span><span class="sxs-lookup"><span data-stu-id="ebec0-126">End of support</span></span><br/> | <span data-ttu-id="ebec0-127">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ebec0-127">Windows�7 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="ebec0-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="ebec0-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="ebec0-129"><dt>Cryptui .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ebec0-129"><dt>Cryptui.lib</dt></span></span> </dl>            |
| <span data-ttu-id="ebec0-130">DLL</span><span class="sxs-lookup"><span data-stu-id="ebec0-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ebec0-131"><dt>Cryptui.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ebec0-131"><dt>Cryptui.dll</dt></span></span> </dl>            |
| <span data-ttu-id="ebec0-132">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="ebec0-132">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ebec0-133">**CryptUIDlgSelectCertificateW** (Unicode) 和 **CryptUIDlgSelectCertificateA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="ebec0-133">**CryptUIDlgSelectCertificateW** (Unicode) and **CryptUIDlgSelectCertificateA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ebec0-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ebec0-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebec0-135">**CRYPTUI \_ SELECTCERTIFICATE \_ 結構**</span><span class="sxs-lookup"><span data-stu-id="ebec0-135">**CRYPTUI\_SELECTCERTIFICATE\_STRUCT**</span></span>](cryptui-selectcertificate-struct.md)
</dt> </dl>






