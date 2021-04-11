---
description: CIMType 限定詞包含描述屬性類型的文字。
ms.assetid: ae65d4c7-2150-489b-a368-fb38c0d1b3be
ms.tgt_platform: multiple
title: CIMType 辨識符號
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIMType
api_type:
- NA
api_location: ''
ms.openlocfilehash: 522f7b3e7f5691e9552dce15b958fdb635fcae06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115868"
---
# <a name="cimtype-qualifier"></a>CIMType 辨識符號

**CIMType** 限定詞包含描述屬性類型的文字。

此文字可以是 MOF 類型，例如 "string" 和 "sint32"，或 CIM 類型，例如 "CIM \_ string" 和 "cim \_ sint32"。 **CIMType** 限定詞與 [**IWbemClassObject：： Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get)方法的 *pvtType* 參數中所使用的屬性類型之間有一對一的對應關係。

這兩個例外狀況如下：

-   [*參考屬性*](gloss-r.md)，其類型為 **CIM \_ 參考**，其中包含 "REF： classname" 值。 Classname 值描述參考屬性的類別類型。
-   具有 **CIM \_ 物件** 類型的内嵌物件屬性。

不過請注意， **CIMType** 限定詞可以和應該用來更精確地輸入參考屬性。 例如，如果屬性永遠參考 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) 類別的實例，其 **CIMType** 限定詞應設定為：


```mof
"ref:Win32_LogicalDisk"
```



根據預設，參考屬性的 **CIMType** 限定詞具有類型 **ref**。

如同參考屬性， **CIMType** 限定詞應該用來以下列語法更精確地輸入内嵌物件屬性：


```mof
"object:EmbedClass"
```



由於 WMI 允許的類型比使用 VT 前置詞的標準常數來表示的類型多 \_ ， **CIMType** 限定詞可協助解讀型別值。 系統會自動新增 **CIMType** 限定詞。 如需詳細資訊，請參閱 [MOF 資料類型](mof-data-types.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>       |
| 最低支援的伺服器<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**標準 WMI 限定詞**](standard-wmi-qualifiers.md)
</dt> <dt>

[WMI 限定詞](wmi-qualifiers.md)
</dt> <dt>

[新增限定詞](adding-a-qualifier.md)
</dt> </dl>

 

