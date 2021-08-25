---
title: 'ResourceLocator. FragmentDialect 屬性 (WSManDisp .h) '
description: 取得或設定在會話物件作業（例如 Session. Get、Session. Put 或 Session. 列舉）中使用 ResourceLocator 時，資源片段方言的語言方言。
ms.assetid: 60b08084-f4b9-4049-b0cd-a7420fcffd7c
ms.tgt_platform: multiple
keywords:
- FragmentDialect 屬性 Windows 遠端管理
- FragmentDialect 屬性 Windows 遠端管理，ResourceLocator 物件
- ResourceLocator 物件 Windows 遠端管理、FragmentDialect 屬性
topic_type:
- apiref
api_name:
- ResourceLocator.FragmentDialect
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2ae7cbbd71b4ccad24ecaa17d0fd635761f661bcd6dc95ebc0345e9164adcd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997298"
---
# <a name="resourcelocatorfragmentdialect-property"></a>ResourceLocator. FragmentDialect 屬性

取得或設定在 [**會話**](session.md)物件作業（例如 [**session. Get**](session-get.md)、 [**session. Put**](session-put.md)或 [**session. 列舉**](session-enumerate.md)）中使用 [**ResourceLocator**](resourcelocator.md)時，[*資源*](windows-remote-management-glossary.md)[*片段*](windows-remote-management-glossary.md)*方言* 的語言方言。 片段代表資源的一個屬性或部分。 您可以提供 [**ResourceLocator**](resourcelocator.md) 物件，而不是在 [**會話**](session.md) 物件作業中指定資源 URI。 此方言會指出哪一個 XML 語言描述處理 [WS-Management 通訊協定](ws-management-protocol.md) 並接收要求之服務的片段。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```VB
ResourceLocator.FragmentDialect As string
```



## <a name="property-value"></a>屬性值

識別 [**FragmentPath**](resourcelocator-fragmentpath.md) 屬性中所使用之語言的 XML 字串。 此方言字串預設為 XPath 1.0 規格。 如需詳細資訊，請參閱 [https://www.w3.org/TR/xpath](https://www.w3.org/TR/xpath)。

## <a name="remarks"></a>備註

[**IWSManResourceLocator：： FragmentDialect**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanresourcelocator-get_fragmentdialect) 是對應的 c + + 屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                 |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                           |
| 標頭<br/>                   | <dl> <dt>WSManDisp。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp .idl</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>WSManDisp .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ResourceLocator**](resourcelocator.md)
</dt> </dl>

 

 





