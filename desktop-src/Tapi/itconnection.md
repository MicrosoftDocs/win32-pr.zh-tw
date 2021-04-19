---
description: ITConnection 介面功能如下所示。
ms.assetid: 44dc39cf-3222-41ed-b29c-df2d32615500
title: 'ITConnection 介面 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a00da80631c0ef4e8186aa36425f18e4d2a62bfc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981403"
---
# <a name="itconnection-interface"></a>ITConnection 介面

\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。 RTC 用戶端 API 提供類似的功能。\]

**ITConnection** 介面提供下列功能：

-   提供會話的位址和存留時間 (TTL) 資訊的存取權。
-   提供頻寬資訊的存取。
-   啟用加密金鑰的操作。

**ITConnection** 介面是藉由在 [**ITConferenceBlob**](itconferenceblob.md)上呼叫 **QueryInterface** 來建立。

## <a name="members"></a>成員

**ITConnection** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。 **ITConnection** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ITConnection** 介面具有這些方法。



| 方法                                                               | 描述                                                                                                                                    |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**取得 \_ AddressType**](itconnection-get-addresstype.md)             | 取得網址類別型。<br/>                                                                                                              |
| [**取得 \_ 頻寬**](itconnection-get-bandwidth.md)                 | 取得頻寬值。<br/>                                                                                                               |
| [**取得 \_ BandwidthModifier**](itconnection-get-bandwidthmodifier.md) | 取得頻寬修飾詞。<br/>                                                                                                        |
| [**取得 \_ NetworkType**](itconnection-get-networktype.md)             | 取得網路類型。<br/>                                                                                                              |
| [**取得 \_ NumAddresses**](itconnection-get-numaddresses.md)           | 取得要用於會話的位址數目。<br/>                                                                            |
| [**取得 \_ StartAddress**](itconnection-get-startaddress.md)           | 取得要用於會話的第一個位址。<br/>                                                                                  |
| [**取得 \_ Ttl**](itconnection-get-ttl.md)                             | 取得位址上傳輸 (TTL) 範圍的 [*存留時間*](t-tapgloss.md) 。<br/> |
| [**GetEncryptionKey**](itconnection-getencryptionkey.md)            | 取得加密金鑰。<br/>                                                                                                            |
| [**put \_ AddressType**](itconnection-put-addresstype.md)             | 設定網址類別型。<br/>                                                                                                              |
| [**put \_ NetworkType**](itconnection-put-networktype.md)             | 設定網路類型。<br/>                                                                                                              |
| [**SetAddressInfo**](itconnection-setaddressinfo.md)                | 設定位址資訊。<br/>                                                                                                           |
| [**SetBandwidthInfo**](itconnection-setbandwidthinfo.md)            | 設定頻寬值。<br/>                                                                                                           |
| [**SetEncryptionKey**](itconnection-setencryptionkey.md)            | 設定解密會話所需的加密金鑰，或用來取得以外部方式取得可用金鑰之機制的指示。<br/>     |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3.0 或更新版本<br/>                                                 |
| 標頭<br/>       | <dl> <dt>Sdpblb。h</dt> </dl>   |
| 程式庫<br/>      | <dl> <dt>Uuid</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

