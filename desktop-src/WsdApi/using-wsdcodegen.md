---
description: 說明使用 WsdCodeGen 建立 WSDAPI 應用程式的流程。
ms.assetid: 8f172e2c-4cd1-4108-9c8d-01a731aca83b
title: 使用 WsdCodeGen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e09bd2b0c8f96d51751aa90bc3206a0824f19b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971817"
---
# <a name="using-wsdcodegen"></a><span data-ttu-id="b40f8-103">使用 WsdCodeGen</span><span class="sxs-lookup"><span data-stu-id="b40f8-103">Using WsdCodeGen</span></span>

<span data-ttu-id="b40f8-104">**使用 WsdCodeGen 建立 WSDAPI 應用程式**</span><span class="sxs-lookup"><span data-stu-id="b40f8-104">**To build a WSDAPI application using WsdCodeGen**</span></span>

1.  <span data-ttu-id="b40f8-105">在 WSDL 檔案中定義裝置主機的功能合約。</span><span class="sxs-lookup"><span data-stu-id="b40f8-105">Define the functional contract for the device host in a WSDL file.</span></span>
2.  <span data-ttu-id="b40f8-106">使用 WsdCodeGen 產生設定檔。</span><span class="sxs-lookup"><span data-stu-id="b40f8-106">Generate a configuration file using WsdCodeGen.</span></span> <span data-ttu-id="b40f8-107">如需詳細資訊，請參閱 [WsdCodeGen 設定檔](wsdcodegen-configuration-file.md) 和 [WsdCodeGen 命令列語法](wsdcodegen-command-line-syntax.md)。</span><span class="sxs-lookup"><span data-stu-id="b40f8-107">For more information, see [WsdCodeGen Configuration File](wsdcodegen-configuration-file.md) and [WsdCodeGen Command Line Syntax](wsdcodegen-command-line-syntax.md).</span></span>
3.  <span data-ttu-id="b40f8-108">開啟產生的設定檔，並視需要修改檔案。</span><span class="sxs-lookup"><span data-stu-id="b40f8-108">Open the generated configuration file and modify the file as required.</span></span> <span data-ttu-id="b40f8-109">如果您要建立用戶端應用程式，則不需要修改或修改。</span><span class="sxs-lookup"><span data-stu-id="b40f8-109">If you are building a client application, little or no modification is required.</span></span> <span data-ttu-id="b40f8-110">如果您要建立主應用程式，請將使用者專屬的設定元素 (例如 [ [**製造商**](manufacturer.md) ] 和 [ [**modelName**](modelname.md) ]) 。</span><span class="sxs-lookup"><span data-stu-id="b40f8-110">If you are building a host application, change the user-specific configuration elements (such as [**manufacturer**](manufacturer.md) and [**modelName**](modelname.md)).</span></span>
4.  <span data-ttu-id="b40f8-111">使用 WsdCodeGen 產生程式碼，並提供設定檔做為輸入。</span><span class="sxs-lookup"><span data-stu-id="b40f8-111">Generate code using WsdCodeGen, providing the configuration file as input.</span></span> <span data-ttu-id="b40f8-112">如需詳細資訊，請參閱 [WsdCodeGen 命令列語法](wsdcodegen-command-line-syntax.md)。</span><span class="sxs-lookup"><span data-stu-id="b40f8-112">For more information, see [WsdCodeGen Command Line Syntax](wsdcodegen-command-line-syntax.md).</span></span>
5.  <span data-ttu-id="b40f8-113">使用產生的程式碼來建立用戶端、主機或兩者。</span><span class="sxs-lookup"><span data-stu-id="b40f8-113">Use the generated code to build a client, host, or both.</span></span>

<span data-ttu-id="b40f8-114">Windows SDK 包含一些範例 WSDL 檔案、WsdCodeGen 設定檔案和產生的程式碼。</span><span class="sxs-lookup"><span data-stu-id="b40f8-114">The Windows SDK includes some sample WSDL files, WsdCodeGen configuration files, and generated code.</span></span> <span data-ttu-id="b40f8-115">如需詳細資訊，請參閱 [WSDAPI 範例](wsdapi-samples.md)。</span><span class="sxs-lookup"><span data-stu-id="b40f8-115">For more information, see [WSDAPI Samples](wsdapi-samples.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b40f8-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="b40f8-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b40f8-117">WSDAPI 範例</span><span class="sxs-lookup"><span data-stu-id="b40f8-117">WSDAPI Samples</span></span>](wsdapi-samples.md)
</dt> </dl>

 

 



