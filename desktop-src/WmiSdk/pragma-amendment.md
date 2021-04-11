---
description: 指示 MOF 編譯器將 MOF 檔案分隔成非語言相關和語言特定版本。
ms.assetid: c1aec33c-b936-4cca-8fcd-7bd088af7116
ms.tgt_platform: multiple
title: pragma 修訂
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pragma
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1269ac1a96617b72852e687b2a38ce8d331ab3e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691527"
---
# <a name="pragma-amendment"></a><span data-ttu-id="fcc16-103">pragma 修訂</span><span class="sxs-lookup"><span data-stu-id="fcc16-103">pragma amendment</span></span>

<span data-ttu-id="fcc16-104">**Pragma 修訂** 預處理器命令會指示 mof 編譯器將 mof 檔案分隔成非語言相關和語言特定版本。</span><span class="sxs-lookup"><span data-stu-id="fcc16-104">The **pragma amendment** preprocessor command directs the MOF compiler to separate a MOF file into language-neutral and language-specific versions.</span></span> <span data-ttu-id="fcc16-105">特定語言的 MOF 檔案會將修改過的限定詞移至特定地區設定的命名空間。</span><span class="sxs-lookup"><span data-stu-id="fcc16-105">The language-specific MOF file moves amended qualifiers to a namespace for a specific locale.</span></span> <span data-ttu-id="fcc16-106">然後，您可以編譯語言特定和語言中性的 MOF 檔案，將類別資訊儲存在 WMI 存放庫中。</span><span class="sxs-lookup"><span data-stu-id="fcc16-106">You then compile the language-specific and language-neutral MOF files to store class information in the WMI repository.</span></span>

## <a name="examples"></a><span data-ttu-id="fcc16-107">範例</span><span class="sxs-lookup"><span data-stu-id="fcc16-107">Examples</span></span>

<span data-ttu-id="fcc16-108">下列範例示範如何建立包含修改過的限定詞的 MOF 檔案。</span><span class="sxs-lookup"><span data-stu-id="fcc16-108">The following example shows how to create a MOF file that contains amended qualifiers.</span></span> <span data-ttu-id="fcc16-109">然後，您可以使用下列命令來編譯 MOF 程式碼：</span><span class="sxs-lookup"><span data-stu-id="fcc16-109">You can then compile the MOF code with the following command:</span></span>

<span data-ttu-id="fcc16-110">**mofcomp.exe** **-mof： Lnmof** **MFL： Lsmof. MFL** **Mastermof. mof**</span><span class="sxs-lookup"><span data-stu-id="fcc16-110">**mofcomp** **-MOF:Lnmof.mof** **-MFL:Lsmof.mfl** **Mastermof.mof**</span></span>

<span data-ttu-id="fcc16-111">此命令會指示 MOF 編譯器從原始的 Mastermof mof 檔案產生兩個 MOF 檔案。</span><span class="sxs-lookup"><span data-stu-id="fcc16-111">The command instructs the MOF compiler to produce two MOF files from the original Mastermof.mof file.</span></span> <span data-ttu-id="fcc16-112">MOF 編譯器會產生一種語言中性版本的 MOF 檔案（稱為 Lnmof），並移除所有語言特定專案。</span><span class="sxs-lookup"><span data-stu-id="fcc16-112">The MOF compiler produces a language-neutral version of the MOF file, called Lnmof.mof, with all language-specific items removed.</span></span> <span data-ttu-id="fcc16-113">編譯器也會建立名為 Lsmof 的第二個特定語言的 MOF 檔案，該檔案只包含您必須當地語系化的專案。</span><span class="sxs-lookup"><span data-stu-id="fcc16-113">The compiler also creates a second, language-specific MOF file called Lsmof.mfl that contains only items that you must localize.</span></span>

> [!Note]  
> <span data-ttu-id="fcc16-114">當您使用 **修訂** 辨識符號或 **pragma 修訂** 命令分割 MOF 檔案時，必須指定 **-MOF** 和 **-MFL** 選項。</span><span class="sxs-lookup"><span data-stu-id="fcc16-114">When you are splitting a MOF file with the **amendment** qualifier or the **pragma amendment** command, you must specify the **-MOF** and **-MFL** options.</span></span> <span data-ttu-id="fcc16-115">否則，編譯器不會產生任何輸出檔。</span><span class="sxs-lookup"><span data-stu-id="fcc16-115">Otherwise, the compiler does not generate any output files.</span></span> <span data-ttu-id="fcc16-116">接著，您必須編譯兩個輸出檔案，才能讓類別資訊可供 WMI 使用。</span><span class="sxs-lookup"><span data-stu-id="fcc16-116">You must then compile the two output files to make the class information available to WMI.</span></span>

 


```mof
#pragma amendment ("MS_409")

[Description("Localized version of MyClass" for American English") :
    Amended, LOCALE(0x409)] 

Class myclass
{
     [DisplayName("User Name") : Amended,
     Description("The Name property contains the name of the user") : 
     Amended, key]
    string Name;

    uint64 Value; // non-localized value field

     [DisplayName("Time Stamp") : Amended,
     Description("This property shows when the object was created") : 
     Amended] 
    uint64 Timestamp;
};
```



## <a name="requirements"></a><span data-ttu-id="fcc16-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="fcc16-117">Requirements</span></span>



| <span data-ttu-id="fcc16-118">需求</span><span class="sxs-lookup"><span data-stu-id="fcc16-118">Requirement</span></span> | <span data-ttu-id="fcc16-119">值</span><span class="sxs-lookup"><span data-stu-id="fcc16-119">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="fcc16-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fcc16-120">Minimum supported client</span></span><br/> | <span data-ttu-id="fcc16-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fcc16-121">Windows Vista</span></span><br/>       |
| <span data-ttu-id="fcc16-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fcc16-122">Minimum supported server</span></span><br/> | <span data-ttu-id="fcc16-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fcc16-123">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fcc16-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fcc16-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcc16-125">預處理器命令</span><span class="sxs-lookup"><span data-stu-id="fcc16-125">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 




