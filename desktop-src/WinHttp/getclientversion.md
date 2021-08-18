---
description: 取得 WPAD 處理引擎的版本。
ms.assetid: f9e9a867-d491-4d46-bbd8-c0c3d8d5b3d6
title: getClientVersion 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- dnsResolveEx
api_type:
- NA
api_location: ''
ms.openlocfilehash: 33aeb4bd59730c48407220fede0cec0a606614f4a9692cd0e9852d56757a7f9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133211"
---
# <a name="getclientversion-function"></a>getClientVersion 函式

取得 WPAD 處理引擎的版本。

## <a name="parameters"></a>參數

<dl> <dt>

*IpAddressList* 
</dt> <dd>

以分號分隔的字串，其中包含 IP 位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

已排序之分號分隔 IP 位址的清單，如果無法排序 IP 位址清單，則為空字串。

## <a name="remarks"></a>備註

此函數目前會傳回1.0 版。

Microsoft 新增了此函式，可讓 IT 系統管理員將其 WPAD 腳本更新為使用不同版本的 WPAD 處理引擎，而不會導致中斷現有的部署。 例如，如果 Microsoft 將函式新增至2.0 版的 WPAD 引擎，則系統管理員可以在嘗試呼叫該函式之前，先檢查版本。 這可讓其腳本與執行 WPAD 引擎1.0 和2.0 版的用戶端搭配使用。

## <a name="examples"></a>範例

``` syntax
getClientVersion();
    returns the appropriate versions number of the WPAD engine.
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[IPv6 感知 Proxy Helper API 定義](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[瀏覽器自動設定檔案格式的 IPv6 擴充功能](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



