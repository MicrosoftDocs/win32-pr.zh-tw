---
title: /app_config 參數
description: /App \_ config 參數會選取應用程式設定模式，可讓您在 IDL 檔案中使用某些 ACF 關鍵字。 使用這個 MIDL 編譯器參數，您可以省略 ACF，並在單一 IDL 檔案中指定介面。
ms.assetid: 8d12a0ed-7eaa-4ebc-a961-b726aefefadc
keywords:
- /app_config switch MIDL
topic_type:
- apiref
api_name:
- /app_config
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 717d5234bd419fec7107a6d983ece026b4558935
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104373241"
---
# <a name="app_config-switch"></a><span data-ttu-id="8ee52-105">/app \_ config 參數</span><span class="sxs-lookup"><span data-stu-id="8ee52-105">/app\_config switch</span></span>

<span data-ttu-id="8ee52-106">**/App \_ config** 參數會選取應用程式設定模式，可讓您在 IDL 檔案中使用某些 ACF 關鍵字。</span><span class="sxs-lookup"><span data-stu-id="8ee52-106">The **/app\_config** switch selects application-configuration mode, which allows you to use some ACF keywords in the IDL file.</span></span> <span data-ttu-id="8ee52-107">使用這個 MIDL 編譯器參數，您可以省略 ACF，並在單一 IDL 檔案中指定介面。</span><span class="sxs-lookup"><span data-stu-id="8ee52-107">With this MIDL compiler switch, you can omit the ACF and specify an interface in a single IDL file.</span></span>

``` syntax
midl /app_config
```

## <a name="switch-options"></a><span data-ttu-id="8ee52-108">切換選項</span><span class="sxs-lookup"><span data-stu-id="8ee52-108">Switch Options</span></span>

<span data-ttu-id="8ee52-109">此參數沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="8ee52-109">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ee52-110">備註</span><span class="sxs-lookup"><span data-stu-id="8ee52-110">Remarks</span></span>

<span data-ttu-id="8ee52-111">Microsoft RPC 支援在 IDL 檔案中使用下列 ACF 屬性：</span><span class="sxs-lookup"><span data-stu-id="8ee52-111">Microsoft RPC supports the use of the following ACF attributes in the IDL file:</span></span>

-   <span data-ttu-id="8ee52-112">隱含 \_ 控制碼</span><span class="sxs-lookup"><span data-stu-id="8ee52-112">Implicit\_handle</span></span>
-   <span data-ttu-id="8ee52-113">自動 \_ 處理</span><span class="sxs-lookup"><span data-stu-id="8ee52-113">Auto\_handle</span></span>
-   <span data-ttu-id="8ee52-114">明確 \_ 控制碼</span><span class="sxs-lookup"><span data-stu-id="8ee52-114">Explicit\_handle</span></span>

<span data-ttu-id="8ee52-115">Microsoft RPC 的未來版本可能會支援在 IDL 檔案中使用其他 ACF 屬性。</span><span class="sxs-lookup"><span data-stu-id="8ee52-115">Future releases of Microsoft RPC may support the use of other ACF attributes in the IDL file.</span></span> <span data-ttu-id="8ee52-116">**/App \_ config** 選項代表憑證-DCE 規格的 Microsoft 擴充功能，因此與 [**/osf**](-osf.md)選項互斥。</span><span class="sxs-lookup"><span data-stu-id="8ee52-116">The **/app\_config** option represents a Microsoft extension to the OSF-DCE specification and, as such, is mutually exclusive with the [**/osf**](-osf.md) option.</span></span>

<span data-ttu-id="8ee52-117">如需 **/app \_ config** 參數的相關詳細資訊，請參閱 [應用程式佈建檔 (ACF)](application-configuration-file-acf-.md) 和 [介面定義 (IDL)](interface-definition-idl-file.md)檔。</span><span class="sxs-lookup"><span data-stu-id="8ee52-117">For more information related to the **/app\_config** switch, see [Application Configuration File (ACF)](application-configuration-file-acf-.md) and [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

## <a name="examples"></a><span data-ttu-id="8ee52-118">範例</span><span class="sxs-lookup"><span data-stu-id="8ee52-118">Examples</span></span>

<span data-ttu-id="8ee52-119">**midl/app \_ config 檔案名 .idl**</span><span class="sxs-lookup"><span data-stu-id="8ee52-119">**midl /app\_config filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="8ee52-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8ee52-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ee52-121">一般 MIDL 命令列語法</span><span class="sxs-lookup"><span data-stu-id="8ee52-121">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




