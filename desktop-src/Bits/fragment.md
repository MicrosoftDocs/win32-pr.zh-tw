---
title: 片段
description: 使用片段封包將上傳檔案的片段傳送至伺服器。
ms.assetid: d6df7e47-a240-4be2-a9c4-24a13e622861
keywords:
- 片段位
topic_type:
- apiref
api_name:
- Fragment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 613acaabc017b9e673d2cba6a64f84db054a4cdc0d73a0639fcf8455edff8298
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528828"
---
# <a name="fragment"></a>片段

使用 **片段** 封包將上傳檔案的片段傳送至伺服器。

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Fragment
BITS-Session-Id: {guid}
Content-Name: filename
Content-Length: length
Content-Range: Bytes range/total-length
Content-Encoding: encoding
```

## <a name="headers"></a>標題

<dl> <dt>

<span id="BITS_POST"></span><span id="bits_post"></span>BITS \_ POST
</dt> <dd>

識別此封包到 BITS 伺服器的位特定動詞。

將遠端 URL 取代為絕對或相對 URI。 通常，將遠端 URL 取代為作業的遠端檔案名。 如需網路負載平衡的考慮，請參閱 [**建立會話**](create-session.md) 封包中的 BITS 主機識別碼標頭。

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-封包類型
</dt> <dd>

將此要求封包識別為片段封包。

</dd> <dt>

<span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>位-會話識別碼
</dt> <dd>

識別伺服器會話的字串 GUID。 將 {guid} 取代為伺服器在 [**建立會話**](ack-for-create-session.md) 回應封包的 Ack 中傳回的會話識別碼。

</dd> <dt>

<span id="Content-Name"></span><span id="content-name"></span><span id="CONTENT-NAME"></span>內容名稱
</dt> <dd>

請僅使用初始片段來指定此標頭。 使用作業中的本機檔案名取代檔案名。 名稱不包含路徑。

</dd> <dt>

<span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>內容長度
</dt> <dd>

以片段主體中傳送的位元組數取代長度。

</dd> <dt>

<span id="Content-Range"></span><span id="content-range"></span><span id="CONTENT-RANGE"></span>內容約制
</dt> <dd>

告訴伺服器要將範圍套用到目的地檔案中。 將範圍取代為目的地檔案中範圍的起始和結束位移。 位移以零為基底。 如果指定的範圍與現有的範圍重迭，則位只會寫入範圍中非重迭的部分;BITS 不會覆寫現有的內容。 例如，如果第一個封包的範圍是0到100，而第二個封包的範圍是50到150，則 BITS 只寫入第二個封包的位元組101至150。 將總長度取代為檔案中的總位元組數。

</dd> <dt>

<span id="Content-Encoding"></span><span id="content-encoding"></span><span id="CONTENT-ENCODING"></span>內容編碼
</dt> <dd>

以用戶端在片段上使用的編碼類型取代編碼。 用戶端必須使用伺服器在 [**建立會話**](ack-for-create-session.md) 回應封包的 Ack Accept-Encoding 標頭中所識別的編碼方式。 伺服器使用編碼類型來解碼片段。 所有片段都必須指定相同的編碼方式。

如果編碼類型為 Identity，請勿傳送此標頭。 BITS 伺服器僅支援身分識別編碼。

</dd> </dl>

## <a name="remarks"></a>備註

片段是在封包主體中傳送的位元組範圍。 用戶端會依順序從位移零開始傳送片段;伺服器不會追蹤非連續的範圍。 如果用戶端傳送非連續的範圍，伺服器會傳回 HTTP 416 (範圍-未] 正確的) 傳回程序代碼，在 [**片段**](ack-for-fragment.md) 回應的 Ack 中。

Content-type *標頭是標準的 HTTP* 1.1 標頭。 如需 *content-type 標頭* 的詳細資訊，請參閱 [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt) 規格。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**適用于片段的 Ack**](ack-for-fragment.md)
</dt> <dt>

[**關閉會話**](close-session.md)
</dt> <dt>

[**建立-會話**](create-session.md)
</dt> </dl>

 

 




