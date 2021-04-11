---
description: 使用者定義的回呼函式，可讓 CryptUIDlgSelectCertificate 函式的呼叫者處理使用者選取要查看的憑證顯示。
ms.assetid: fdb9e9e0-02f1-42e0-9a11-204d916a1a88
title: PFNCCERTDISPLAYPROC 回呼函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PFNCCERTDISPLAYPROC
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 7371e983b339ff8bfa9edb1b7fb795ab64596a98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026807"
---
# <a name="pfnccertdisplayproc-callback-function"></a><span data-ttu-id="9b2a5-103">PFNCCERTDISPLAYPROC 回呼函式</span><span class="sxs-lookup"><span data-stu-id="9b2a5-103">PFNCCERTDISPLAYPROC callback function</span></span>

<span data-ttu-id="9b2a5-104">**PFNCCERTDISPLAYPROC** 函式是使用者定義的回呼函式，可讓 [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md)函式的呼叫者處理使用者選取要查看的憑證顯示。</span><span class="sxs-lookup"><span data-stu-id="9b2a5-104">The **PFNCCERTDISPLAYPROC** function is a user-defined callback function that allows the caller of the [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md) function to handle the display of certificates that the user selects to view.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b2a5-105">語法</span><span class="sxs-lookup"><span data-stu-id="9b2a5-105">Syntax</span></span>


```C++
BOOL WINAPI * PFNCCERTDISPLAYPROC(
  _In_ PCCERT_CONTEXT pCertContext,
  _In_ HWND           hWndSelCertDlg,
  _In_ void           *pvCallbackData
);
```



## <a name="parameters"></a><span data-ttu-id="9b2a5-106">參數</span><span class="sxs-lookup"><span data-stu-id="9b2a5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b2a5-107">*pCertCoNtext* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9b2a5-107">*pCertContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b2a5-108">憑證 [**\_ 內容**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) 結構的指標，表示要顯示的憑證。</span><span class="sxs-lookup"><span data-stu-id="9b2a5-108">A pointer to a [**CERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) structure that represents the certificate to display.</span></span>

</dd> <dt>

<span data-ttu-id="9b2a5-109">*hWndSelCertDlg* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9b2a5-109">*hWndSelCertDlg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b2a5-110">對話方塊的控制碼，此對話方塊會選取憑證來進行查看。</span><span class="sxs-lookup"><span data-stu-id="9b2a5-110">A handle to the dialog box from which the certificate was selected for viewing.</span></span>

</dd> <dt>

<span data-ttu-id="9b2a5-111">*pvCallbackData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9b2a5-111">*pvCallbackData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b2a5-112">回呼函數所使用的其他資料。</span><span class="sxs-lookup"><span data-stu-id="9b2a5-112">Additional data used by the callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b2a5-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="9b2a5-113">Return value</span></span>

<span data-ttu-id="9b2a5-114">此函式會傳回 **TRUE** ，表示它會處理憑證的顯示，而且對話方塊不應顯示憑證。</span><span class="sxs-lookup"><span data-stu-id="9b2a5-114">This function returns **TRUE** to indicate that it handles display of the certificate and that the dialog box should not display the certificate.</span></span> <span data-ttu-id="9b2a5-115">如果此函數傳回 **FALSE**，則對話方塊會顯示憑證。</span><span class="sxs-lookup"><span data-stu-id="9b2a5-115">If this function returns **FALSE**, the dialog box displays the certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b2a5-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="9b2a5-116">Requirements</span></span>



| <span data-ttu-id="9b2a5-117">需求</span><span class="sxs-lookup"><span data-stu-id="9b2a5-117">Requirement</span></span> | <span data-ttu-id="9b2a5-118">值</span><span class="sxs-lookup"><span data-stu-id="9b2a5-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9b2a5-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9b2a5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9b2a5-120">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9b2a5-120">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="9b2a5-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9b2a5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9b2a5-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9b2a5-122">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 




