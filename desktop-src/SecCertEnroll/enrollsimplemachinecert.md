---
description: 使用範本、憑證顯示名稱和憑證描述，在證書階層中註冊電腦。
ms.assetid: d9e01767-f6e8-4fd6-a848-8d5acf57407e
title: enrollSimpleMachineCert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8582bc73fdee7e8be6b2cff8d0aec81b84487307
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106977064"
---
# <a name="enrollsimplemachinecert"></a><span data-ttu-id="12f30-103">enrollSimpleMachineCert</span><span class="sxs-lookup"><span data-stu-id="12f30-103">enrollSimpleMachineCert</span></span>

<span data-ttu-id="12f30-104">EnrollSimpleMachineCert 範例會使用範本、憑證顯示名稱和憑證描述，在證書階層中註冊電腦。</span><span class="sxs-lookup"><span data-stu-id="12f30-104">The enrollSimpleMachineCert sample enrolls a computer in a certificate hierarchy by using a template, a certificate display name, and the certificate description.</span></span>

## <a name="location"></a><span data-ttu-id="12f30-105">Location</span><span class="sxs-lookup"><span data-stu-id="12f30-105">Location</span></span>

<span data-ttu-id="12f30-106">當您安裝 Microsoft Windows 軟體開發套件 (SDK) 時，根據預設，系統會在 *% ProgramFiles%* \\ Microsoft sdk \\ Windows \\ 7.0 \\ 範例 \\ 安全性 \\ X509 憑證註冊 \\ VC \\ EnrollSimpleMachineCert 資料夾中安裝 c + + 版本的範例。</span><span class="sxs-lookup"><span data-stu-id="12f30-106">When you install the Microsoft Windows Software Development Kit (SDK), a C++ version of the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\EnrollSimpleMachineCert folder.</span></span> <span data-ttu-id="12f30-107">VBScript 版本安裝在 *% ProgramFiles%* \\ Microsoft sdk \\ Windows \\ 7.0 版 \\ 範例 \\ 安全性 \\ X509 憑證註冊 \\ VBS \\ EnrollSimpleMachineCert 資料夾中。</span><span class="sxs-lookup"><span data-stu-id="12f30-107">A VBScript version is installed in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VBS\\EnrollSimpleMachineCert folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="12f30-108">討論</span><span class="sxs-lookup"><span data-stu-id="12f30-108">Discussion</span></span>

<span data-ttu-id="12f30-109">EnrollSimpleMachineCert 範例：</span><span class="sxs-lookup"><span data-stu-id="12f30-109">The enrollSimpleMachineCert sample:</span></span>

1.  <span data-ttu-id="12f30-110">處理命令列引數。</span><span class="sxs-lookup"><span data-stu-id="12f30-110">Processes the command line arguments.</span></span> <span data-ttu-id="12f30-111">命令列應該包含範本的名稱、憑證顯示名稱和憑證描述。</span><span class="sxs-lookup"><span data-stu-id="12f30-111">The command line should contain the name of the template, a certificate display name, and a certificate description.</span></span>
2.  <span data-ttu-id="12f30-112">建立 [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) 物件，並使用命令列上指定的範本將它初始化。</span><span class="sxs-lookup"><span data-stu-id="12f30-112">Creates an [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object and initializes it by using the template specified on the command line.</span></span> <span data-ttu-id="12f30-113">第一個參數的 CoNtextAdministratorForceMachine 值指定由代表電腦的系統管理員要求憑證。</span><span class="sxs-lookup"><span data-stu-id="12f30-113">The ContextAdministratorForceMachine value for the first parameter specifies that the certificate is being requested by an administrator acting on behalf of a computer.</span></span>
3.  <span data-ttu-id="12f30-114">將顯示名稱和描述新增至註冊物件。</span><span class="sxs-lookup"><span data-stu-id="12f30-114">Adds the display name and description to the enrollment object.</span></span>
4.  <span data-ttu-id="12f30-115">嘗試註冊憑證要求，並檢查進程的狀態。</span><span class="sxs-lookup"><span data-stu-id="12f30-115">Attempts to enroll the certificate request and checks the status of the process.</span></span> <span data-ttu-id="12f30-116">CheckEnrollStatus 函式定義于 enrollCommon .cpp 中。</span><span class="sxs-lookup"><span data-stu-id="12f30-116">The checkEnrollStatus function is defined in enrollCommon.cpp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="12f30-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="12f30-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12f30-118">使用包含的範例</span><span class="sxs-lookup"><span data-stu-id="12f30-118">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 



