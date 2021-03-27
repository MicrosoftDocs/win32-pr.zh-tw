---
description: 就內部而言，中繼檔是稱為中繼檔記錄的可變長度結構陣列。
ms.assetid: 222f9b8b-d759-49f9-a3ea-ac59f85263b8
title: 關於中繼檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdba8b3c0a13c6c5799563b05e189829a0734427
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691475"
---
# <a name="about-metafiles"></a><span data-ttu-id="e9db5-103">關於中繼檔</span><span class="sxs-lookup"><span data-stu-id="e9db5-103">About Metafiles</span></span>

<span data-ttu-id="e9db5-104">就內部而言，中繼檔是稱為 *中繼檔記錄* 的可變長度結構陣列。</span><span class="sxs-lookup"><span data-stu-id="e9db5-104">Internally, a metafile is an array of variable-length structures called *metafile records*.</span></span> <span data-ttu-id="e9db5-105">中繼檔中的第一筆記錄會指定一般資訊，例如圖片建立所在的裝置解析度、圖片的大小等等。</span><span class="sxs-lookup"><span data-stu-id="e9db5-105">The first records in the metafile specify general information such as the resolution of the device on which the picture was created, the dimensions of the picture, and so on.</span></span> <span data-ttu-id="e9db5-106">其餘記錄（構成任何中繼檔的大量）會對應至圖形裝置介面， (需要用來繪製圖片的 GDI) 函數。</span><span class="sxs-lookup"><span data-stu-id="e9db5-106">The remaining records, which constitute the bulk of any metafile, correspond to the graphics device interface (GDI) functions required to draw the picture.</span></span> <span data-ttu-id="e9db5-107">建立特殊的中繼檔裝置內容之後，這些記錄會儲存在中繼檔中。</span><span class="sxs-lookup"><span data-stu-id="e9db5-107">These records are stored in the metafile after a special metafile device context is created.</span></span> <span data-ttu-id="e9db5-108">然後，此中繼檔裝置內容會用於建立圖片所需的所有繪圖作業。</span><span class="sxs-lookup"><span data-stu-id="e9db5-108">This metafile device context is then used for all drawing operations required to create the picture.</span></span> <span data-ttu-id="e9db5-109">當系統處理與中繼檔 DC 相關聯的 GDI 函式時，它會將函式轉換為適當的資料，並將此資料儲存在附加至中繼檔的記錄中。</span><span class="sxs-lookup"><span data-stu-id="e9db5-109">When the system processes a GDI function associated with a metafile DC, it converts the function into the appropriate data and stores this data in a record appended to the metafile.</span></span>

<span data-ttu-id="e9db5-110">在圖片完成並將最後一筆記錄儲存在中繼檔中之後，您可以透過下列方式將中繼檔傳遞給另一個應用程式：</span><span class="sxs-lookup"><span data-stu-id="e9db5-110">After a picture is complete and the last record is stored in the metafile, you can pass the metafile to another application by:</span></span>

-   <span data-ttu-id="e9db5-111">使用剪貼簿</span><span class="sxs-lookup"><span data-stu-id="e9db5-111">Using the clipboard</span></span>
-   <span data-ttu-id="e9db5-112">將它內嵌在另一個檔案中</span><span class="sxs-lookup"><span data-stu-id="e9db5-112">Embedding it within another file</span></span>
-   <span data-ttu-id="e9db5-113">將其儲存在磁片上</span><span class="sxs-lookup"><span data-stu-id="e9db5-113">Storing it on disk</span></span>
-   <span data-ttu-id="e9db5-114">重複播放</span><span class="sxs-lookup"><span data-stu-id="e9db5-114">Playing it repeatedly</span></span>

<span data-ttu-id="e9db5-115">中繼檔會在其記錄轉換成裝置命令並由適當的裝置處理時 *播放* 。</span><span class="sxs-lookup"><span data-stu-id="e9db5-115">A metafile is *played* when its records are converted to device commands and processed by the appropriate device.</span></span>

<span data-ttu-id="e9db5-116">中繼檔有兩種類型：</span><span class="sxs-lookup"><span data-stu-id="e9db5-116">There are two types of metafiles:</span></span>

-   [<span data-ttu-id="e9db5-117">增強格式的中繼檔</span><span class="sxs-lookup"><span data-stu-id="e9db5-117">Enhanced-format metafiles</span></span>](enhanced-format-metafiles.md)
-   [<span data-ttu-id="e9db5-118">Windows-格式中繼檔</span><span class="sxs-lookup"><span data-stu-id="e9db5-118">Windows-format metafiles</span></span>](windows-format-metafiles.md)

 

 



