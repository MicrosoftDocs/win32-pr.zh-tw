---
description: WMI 中的別名是類別或類別實例中，位於受控物件格式 (MOF) 檔中其他位置的符號參考。
ms.assetid: bf4981dc-3aab-46c5-bf02-48132ccec8c2
ms.tgt_platform: multiple
title: 建立 WMI 別名
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fdd538e113f227eac4980855ea0035e839b92fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106975031"
---
# <a name="creating-a-wmi-alias"></a><span data-ttu-id="641b8-103">建立 WMI 別名</span><span class="sxs-lookup"><span data-stu-id="641b8-103">Creating a WMI Alias</span></span>

<span data-ttu-id="641b8-104">WMI 中的 [*別名*](gloss-a.md) 是類別或類別實例中，位於受控物件格式 (MOF) 檔中其他位置的符號參考。</span><span class="sxs-lookup"><span data-stu-id="641b8-104">An [*alias*](gloss-a.md) in WMI is a symbolic reference in either a class or a class instance located elsewhere in a Managed Object Format (MOF) file.</span></span> <span data-ttu-id="641b8-105">MOF 編譯器會使用別名來建立類別和實例之間的參考。</span><span class="sxs-lookup"><span data-stu-id="641b8-105">The MOF compiler uses aliases to establish references between classes and instances.</span></span> <span data-ttu-id="641b8-106">編譯器會將別名解析為它們所參考的類別，因此別名名稱無法在已編譯的程式碼中使用。</span><span class="sxs-lookup"><span data-stu-id="641b8-106">The compiler resolves aliases to the classes to which they refer, so alias names are not available in compiled code.</span></span> <span data-ttu-id="641b8-107">因此，用戶端應用程式無法使用別名來參考類別。</span><span class="sxs-lookup"><span data-stu-id="641b8-107">As a result, client applications cannot refer to classes using aliases.</span></span>

> [!Note]  
> <span data-ttu-id="641b8-108">WMI 支援向前參考，但不支援迴圈別名。</span><span class="sxs-lookup"><span data-stu-id="641b8-108">WMI supports forward referencing but not circular aliases.</span></span>

 

<span data-ttu-id="641b8-109">別名的範圍僅限於您在其中宣告別名的 MOF 檔案內。</span><span class="sxs-lookup"><span data-stu-id="641b8-109">An alias has scope only within the MOF file in which you declare the alias.</span></span> <span data-ttu-id="641b8-110">因此，您通常會使用別名作為較長物件路徑的快捷方式。</span><span class="sxs-lookup"><span data-stu-id="641b8-110">Therefore, you typically use an alias as a shortcut to a lengthy object path.</span></span>

<span data-ttu-id="641b8-111">**若要定義別名**</span><span class="sxs-lookup"><span data-stu-id="641b8-111">**To define an alias**</span></span>

1.  <span data-ttu-id="641b8-112">將 "as $*aliasname*" 片語新增至實例或類別宣告。</span><span class="sxs-lookup"><span data-stu-id="641b8-112">Add the phrase "as $*aliasname*" to the instance or class declaration.</span></span>
2.  <span data-ttu-id="641b8-113">別名名稱會遵循與實例和類別名稱相同的規則，但別名名稱的開頭必須是貨幣符號 ($) 。</span><span class="sxs-lookup"><span data-stu-id="641b8-113">Alias names follow the same rules as instance and class names, except that alias names must begin with a dollar sign ($).</span></span> <span data-ttu-id="641b8-114">底線可出現在初始字元之後的別名名稱中。</span><span class="sxs-lookup"><span data-stu-id="641b8-114">Underscores can appear in an alias name following the initial character.</span></span>

<span data-ttu-id="641b8-115">下列程式碼範例說明如何在類別定義中使用別名。</span><span class="sxs-lookup"><span data-stu-id="641b8-115">The following code example describes how to use an alias in a class definition.</span></span>

``` syntax
class MyClass as $MyClassAlias
{
};
instance of MyClass as $MyInstanceAlias
{
};
```

<span data-ttu-id="641b8-116">下列程式碼範例說明如何使用別名做為物件路徑的符號參考。</span><span class="sxs-lookup"><span data-stu-id="641b8-116">The following code examples describe how to use an alias as a symbolic reference to an object path.</span></span> <span data-ttu-id="641b8-117">這些範例會宣告兩個類別來描述磁片： Disk 類別指出磁碟機號，而 DiskRef 類別指出磁片路徑。</span><span class="sxs-lookup"><span data-stu-id="641b8-117">These examples declare two classes to describe a disk: the Disk class to indicate the drive letter and the DiskRef class to indicate the disk path.</span></span> <span data-ttu-id="641b8-118">系統會為磁片類別實例定義別名。</span><span class="sxs-lookup"><span data-stu-id="641b8-118">An alias is defined for the Disk class instance.</span></span> <span data-ttu-id="641b8-119">此別名會當做 DiskRef 實例中 PathToDisk 屬性的值使用。</span><span class="sxs-lookup"><span data-stu-id="641b8-119">This alias is used as the value for the PathToDisk property in the DiskRef instance.</span></span>

``` syntax
class Disk {
    [key]  string    DriveLetter;
};

class DiskRef 
{
    [key]  string    MyKey;
    Disk   ref       PathToDisk;
};

instance of Disk as $DiskAlias 
{
    DriveLetter = "c";
};

instance of DiskRef
{
    MyKey      =  "hello";
    PathToDisk = $DiskAlias;
};
```

## <a name="related-topics"></a><span data-ttu-id="641b8-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="641b8-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="641b8-121">建立類別</span><span class="sxs-lookup"><span data-stu-id="641b8-121">Creating a Class</span></span>](creating-a-class.md)
</dt> </dl>

 

 



