---
description: 用來設定 CAPICOM 元件。
title: Settings 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Settings
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 27042f9602167f3eb0c1272f7c19fa1170abab40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998630"
---
# <a name="settings-object-cryptography"></a>設定物件 (密碼編譯) 

\[[ **設定** ] 物件可用於 [需求] 區段中指定的作業系統。\]

**Settings** 物件是用來設定 CAPICOM 元件。

## <a name="members"></a>成員

**Settings** 物件具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Settings** 物件具有這些屬性。



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">屬性</th>
<th style="text-align: left;">存取類型</th>
<th style="text-align: left;">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="settings-activedirectorysearchlocation.md"><strong>ActiveDirectorySearchLocation</strong></a><br/></td>
<td style="text-align: left;">讀取/寫入<br/></td>
<td style="text-align: left;">設定或抓取 Active Directory 搜尋位置。 預設不會指定初始位置。 如果未指定位置，則會搜尋通用類別目錄，然後搜尋預設網域。 搜尋會判斷使用者憑證屬性是否在該位置發佈。<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="settings-enablepromptforcertificateui.md"><strong>EnablePromptForCertificateUI</strong></a><br/></td>
<td style="text-align: left;">讀取/寫入<br/></td>
<td style="text-align: left;">設定或取得布林值，這個值會指出是否可以使用使用者介面提示輸入簽署者或寄件者的身分識別。 <br/>
<blockquote>
[!Note]<br />
設定這個屬性並不會停用從 web 應用程式完成任何私密金鑰使用之前所產生的警告。
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>備註

您可以建立 **設定** 物件，而且可以安全地進行腳本處理。 **Settings** 物件的 PROGID 是 CAPICOM。設定。1。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**加密物件**](cryptography-objects.md)
</dt> </dl>

 

 




