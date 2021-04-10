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
# <a name="pragma-amendment"></a>pragma 修訂

**Pragma 修訂** 預處理器命令會指示 mof 編譯器將 mof 檔案分隔成非語言相關和語言特定版本。 特定語言的 MOF 檔案會將修改過的限定詞移至特定地區設定的命名空間。 然後，您可以編譯語言特定和語言中性的 MOF 檔案，將類別資訊儲存在 WMI 存放庫中。

## <a name="examples"></a>範例

下列範例示範如何建立包含修改過的限定詞的 MOF 檔案。 然後，您可以使用下列命令來編譯 MOF 程式碼：

**mofcomp.exe** **-mof： Lnmof** **MFL： Lsmof. MFL** **Mastermof. mof**

此命令會指示 MOF 編譯器從原始的 Mastermof mof 檔案產生兩個 MOF 檔案。 MOF 編譯器會產生一種語言中性版本的 MOF 檔案（稱為 Lnmof），並移除所有語言特定專案。 編譯器也會建立名為 Lsmof 的第二個特定語言的 MOF 檔案，該檔案只包含您必須當地語系化的專案。

> [!Note]  
> 當您使用 **修訂** 辨識符號或 **pragma 修訂** 命令分割 MOF 檔案時，必須指定 **-MOF** 和 **-MFL** 選項。 否則，編譯器不會產生任何輸出檔。 接著，您必須編譯兩個輸出檔案，才能讓類別資訊可供 WMI 使用。

 


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



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>       |
| 最低支援的伺服器<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[預處理器命令](preprocessor-commands.md)
</dt> </dl>

 

 




