---
title: /protocol 參數
description: /Protocol 參數會指定產生的存根所支援的網路通訊協定。
ms.assetid: b565b30c-72e5-442b-9588-324b9041524b
keywords:
- /protocol 參數 MIDL
topic_type:
- apiref
api_name:
- /protocol
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9770fa94d010e21dcbd2a5574a0cffe29273a23
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104313023"
---
# <a name="protocol-switch"></a>/protocol 參數

**/Protocol** 參數會指定產生的存根所支援的網路通訊協定。

``` syntax
midl /protocol (dce | ndr64 | all)
```

## <a name="switch-options"></a>切換選項

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="dce"></span><span id="DCE"></span>

<span id="dce"></span><span id="DCE"></span>dce * * * *


</dt> <dd>

產生的存根僅支援 DCE 通訊協定。

</dd> <dt>

<span id="ndr64"></span><span id="NDR64"></span>

<span id="ndr64"></span><span id="NDR64"></span>ndr64****


</dt> <dd>

產生的存根僅支援 Microsoft NDR64 通訊協定。

</dd> <dt>

<span id="all"></span><span id="ALL"></span>

<span id="all"></span><span id="ALL"></span>全部 * * * *


</dt> <dd>

產生的存根支援指定環境的所有可用通訊協定。

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>備註

RPC 會根據嚴格的線路通訊協定（也稱為傳輸語法）來封送處理和拆收資料，以定義資料線路的標記法，例如封送處理資料成員的順序、網路上的資料對齊方式、資料隨附的額外資訊，還有其他資訊。 Microsoft RPC 與憑證 DCE 的 NDR (網路資料表示) 通訊協定相容。 在 Windows XP 的64位版本中，Microsoft 引進了針對傳輸64位資料優化的實驗性通訊協定 NDR64。 NDR64 與 DCE 通訊協定沒有回溯相容性。

**Dce** 通訊協定與憑證 DCE 的 NDR 傳輸語法相容。 此通訊協定已針對傳輸32位資料進行優化。

目前只有在搭配 [**/win64**](-win64.md)參數使用時，才支援 **ndr64** 通訊協定。 如果僅 ndr64 用戶端嘗試連線到僅限 dce 的伺服器，反之亦然，則會使用 RPC \_ S \_ 不支援的非 \_ 交易 \_ SYN 來拒絕呼叫。

**All** 選項會建立可使用任何可用通訊協定的存根。 若為32位的存根，目前唯一可用的通訊協定為 DCE。 針對使用 [**/win64**](-win64.md) 參數建立的64位存根，可使用 DCE 和 NDR64。

## <a name="examples"></a>範例

**midl/protocol 所有/win64 的檔案名 .idl**

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**/<system>**](-system-.md)
</dt> </dl>

 

 




