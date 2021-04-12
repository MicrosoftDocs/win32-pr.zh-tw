---
description: 在 Winsock 應用程式中，通訊端描述項不是檔案描述項，而且必須與 Winsock 函數搭配使用。
ms.assetid: bc434b35-9231-4b03-bc8f-cf59aaeb821e
title: 通訊端資料類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea031032e0d05abc02f7c3c948477c7fe9a1d1de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319803"
---
# <a name="socket-data-type"></a><span data-ttu-id="1d29c-103">通訊端資料類型</span><span class="sxs-lookup"><span data-stu-id="1d29c-103">Socket Data Type</span></span>

<span data-ttu-id="1d29c-104">在 Winsock 應用程式中，通訊端描述項不是檔案描述項，而且必須與 Winsock 函數搭配使用。</span><span class="sxs-lookup"><span data-stu-id="1d29c-104">In Winsock applications, a socket descriptor is not a file descriptor and must be used with the Winsock functions.</span></span>

<span data-ttu-id="1d29c-105">在 UNIX 中，通訊端描述項是由標準的檔案描述項表示。</span><span class="sxs-lookup"><span data-stu-id="1d29c-105">In UNIX, a socket descriptor is represented by a standard file descriptor.</span></span> <span data-ttu-id="1d29c-106">因此，UNIX 上的通訊端描述項可以傳遞給任何標準的檔案 i/o 函式 (讀取和寫入，例如) 。</span><span class="sxs-lookup"><span data-stu-id="1d29c-106">As a result, a socket descriptor on UNIX may be passed to any of the standard file I/O functions (read and write, for example).</span></span>

<span data-ttu-id="1d29c-107">此外，UNIX 中的所有控制碼（包括通訊端控制碼）都是小型的非負整數，而某些應用程式會假設這會是 true。</span><span class="sxs-lookup"><span data-stu-id="1d29c-107">Furthermore, all handles in UNIX, including socket handles, are small, non-negative integers, and some applications make assumptions that this will be true.</span></span>

<span data-ttu-id="1d29c-108">Windows 通訊端控制碼沒有任何限制，除了值不正確 \_ 通訊端不是有效的通訊端。</span><span class="sxs-lookup"><span data-stu-id="1d29c-108">Windows Sockets handles have no restrictions, other than that the value INVALID\_SOCKET is not a valid socket.</span></span> <span data-ttu-id="1d29c-109">通訊端控制碼可能會採用範圍0到無效 \_ 通訊端-1 的任何值。</span><span class="sxs-lookup"><span data-stu-id="1d29c-109">Socket handles may take any value in the range 0 to INVALID\_SOCKET–1.</span></span>

<span data-ttu-id="1d29c-110">因為 **通訊端** 類型不帶正負號，編譯現有的原始程式碼（例如 UNIX 環境）可能會導致編譯器警告有關簽署/不帶正負號的資料類型不符。</span><span class="sxs-lookup"><span data-stu-id="1d29c-110">Because the **SOCKET** type is unsigned, compiling existing source code from, for example, a UNIX environment may lead to compiler warnings about signed/unsigned data type mismatches.</span></span>

<span data-ttu-id="1d29c-111">這表示，在 [**通訊端**](/windows/desktop/api/Winsock2/nf-winsock2-socket) 和 [**接受**](/windows/desktop/api/Winsock2/nf-winsock2-accept) 函式傳回時，不應藉由比較傳回值與-1 來檢查錯誤，或查看值是否為負面 (UNIX) 的常見和合法方法。</span><span class="sxs-lookup"><span data-stu-id="1d29c-111">This means, for example, that checking for errors when the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) and [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) functions return should not be done by comparing the return value with –1, or seeing if the value is negative (both common and legal approaches in UNIX).</span></span> <span data-ttu-id="1d29c-112">相反地，應用程式應該使用在 \_ *Winsock2* 標頭檔中定義的資訊清單常數無效通訊端。</span><span class="sxs-lookup"><span data-stu-id="1d29c-112">Instead, an application should use the manifest constant INVALID\_SOCKET as defined in the *Winsock2.h* header file.</span></span> <span data-ttu-id="1d29c-113">例如：</span><span class="sxs-lookup"><span data-stu-id="1d29c-113">For example:</span></span>

<span data-ttu-id="1d29c-114">一般 BSD UNIX 樣式</span><span class="sxs-lookup"><span data-stu-id="1d29c-114">Typical BSD UNIX Style</span></span>


```C++
s = socket(...);
if (s == -1)    /* or s < 0 */
    {/*...*/}
```



<span data-ttu-id="1d29c-115">慣用樣式</span><span class="sxs-lookup"><span data-stu-id="1d29c-115">Preferred Style</span></span>


```C++
s = socket(...);
if (s == INVALID_SOCKET)
    {/*...*/}
```



## <a name="related-topics"></a><span data-ttu-id="1d29c-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="1d29c-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d29c-117">將通訊端應用程式移植到 Winsock</span><span class="sxs-lookup"><span data-stu-id="1d29c-117">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="1d29c-118">Winsock 程式設計考慮</span><span class="sxs-lookup"><span data-stu-id="1d29c-118">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> </dl>

 

 



