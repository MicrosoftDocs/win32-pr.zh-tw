---
description: PNRP 會使用 WSALookupServiceNext 函數來比對 WSALookupServiceBegin 先前呼叫中所指定的查詢。
ms.assetid: b3e1abf4-ff59-481d-b96e-f8916a47cd52
title: PNRP 和 WSALookupServiceNext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 398beca2f16e4920ab7fbe43bb648cbc22d9f336
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980986"
---
# <a name="pnrp-and-wsalookupservicenext"></a>PNRP 和 WSALookupServiceNext

PNRP 會使用 [**WSALookupServiceNext**](winsock-nsp-reference-links.md) 函數來比對 **WSALookupServiceBegin** 先前呼叫中所指定的查詢。 **WSALookupServiceNext** 函式的結果是由在初始 **WSALookupServiceBegin** 函式呼叫中傳遞的 **WSAQUERYSET** 結構中的設定所決定。 此函式是用來執行下列兩個函數：

-   將對等名稱解析為地址清單
-   列舉網路雲

您可以使用 [**WSANSPIoctl**](winsock-nsp-reference-links.md)，以非同步方式使用 lookup 服務。 如需以非同步方式使用查閱服務函數的詳細資訊，請參閱 [PNRP 和 WSANSPIoctl](pnrp-and-wsanspioctl.md)。

[**WSALookupServiceNext**](winsock-nsp-reference-links.md)函式會封鎖，即使呼叫 **WSANSPIoctl** 也是一樣。 在呼叫 **WSALookupServiceNext** 之前，應用程式必須等到收到通知（如果封鎖發生問題）。

## <a name="resolving-a-peer-name-to-a-list-of-addresses"></a>將對等名稱解析為地址清單

將對等名稱解析為地址清單時，在 *lpqsResults* 參數中傳回的 [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md)結構會包含下列值：

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

傳回結構的大小。

</dd> <dt>

<span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**
</dt> <dd>

傳回對等名稱，如果 **LUP \_ 傳回 \_ 名稱**，則會指定 **LUP \_ return \_ ALL** 或 **Null** 。

</dd> <dt>

<span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**
</dt> <dd>

傳回 **SVCID \_ PNRPNAME**。

</dd> <dt>

<span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**
</dt> <dd>

傳回 **Null**。

</dd> <dt>

<span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**
</dt> <dd>

傳回批註-如果 **LUP 傳回 \_ \_ 批註**、 **LUP 傳回 \_ \_ 全部**，或指定 **Null** 。

</dd> <dt>

<span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**
</dt> <dd>

傳回 **NS \_ PNRPNAME**。

</dd> <dt>

<span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**
</dt> <dd>

傳回 **NS \_ 提供者 \_ PNRPNAME**。

</dd> <dt>

<span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszCoNtext**
</dt> <dd>

如果指定了 LUP 傳回 **\_ \_ 名稱**、LUP 傳回 **\_ \_ 全部** 或 **Null** ，則會傳回雲端名稱。

</dd> <dt>

<span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**
</dt> <dd>

傳回零 (0) 。

</dd> <dt>

<span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**
</dt> <dd>

傳回 **Null**。

</dd> <dt>

<span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**
</dt> <dd>

傳回 CSADDR 資訊陣列中的專案數 \_ （如果 **LUP 傳回 \_ \_ ADDR**、 **LUP \_ RETURN \_ ALL** 或 **Null** ）。 此值和 **lpcsaBuffer** 中的資訊是此結構中所傳回信息的金鑰位。

</dd> <dt>

<span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**
</dt> <dd>

\_如果 **LUP 傳回 \_ \_ ADDR**、 **LUP \_ RETURN \_ ALL** 或 **Null** ，則傳回 CSADDR 資訊結構陣列的指標。 這個緩衝區和 **dwNumberOfCsAddrs** 中的值是此結構中所傳回的金鑰資訊位。

</dd> <dt>

<span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**
</dt> <dd>

傳回零 (0) 。

</dd> <dt>

<span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**
</dt> <dd>

傳回 **Null**。

</dd> </dl>

## <a name="enumerating-network-clouds"></a>列舉網路雲

列舉雲端時， *lpqsResults* 參數中所傳回的 [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md)結構包含下列值：

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

傳回結構的大小。

</dd> <dt>

<span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**
</dt> <dd>

傳回雲端名稱-如果 **LUP 傳回 \_ \_ 名稱**，則會指定 **LUP \_ return \_ ALL** 或 **Null** 。

</dd> <dt>

<span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**
</dt> <dd>

傳回 **SVCID \_ PNRPCLOUD**。

</dd> <dt>

<span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**
</dt> <dd>

傳回 **Null**。

</dd> <dt>

<span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**
</dt> <dd>

傳回 **Null**。

</dd> <dt>

<span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**
</dt> <dd>

傳回 **NS \_ PNRPCLOUD**。

</dd> <dt>

<span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**
</dt> <dd>

傳回 **NS \_ 提供者 \_ PNRPCLOUD**。

</dd> <dt>

<span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszCoNtext**
</dt> <dd>

傳回 **Null**。

</dd> <dt>

<span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**
</dt> <dd>

傳回零 (0) 。

</dd> <dt>

<span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**
</dt> <dd>

傳回 **Null**。

</dd> <dt>

<span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**
</dt> <dd>

傳回零 (0) 。

</dd> <dt>

<span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**
</dt> <dd>

傳回 **Null**。

</dd> <dt>

<span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**
</dt> <dd>

傳回零 (0) 。

</dd> <dt>

<span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**
</dt> <dd>

傳回指向 [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo)結構之 [**BLOB**](winsock-nsp-reference-links.md)結構的指標，如果 **LUP 傳回 \_ \_ BLOB**、 **LUP 傳回 \_ \_ 全部**，或指定 **Null** 。

</dd> </dl>

## <a name="pnrpcloudinfo-structure"></a>PNRPCLOUDINFO 結構

列舉雲端名稱時， [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) 結構中會傳回下列值：

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**
</dt> <dd>

此結構的大小。

</dd> <dt>

<span id="Cloud"></span><span id="cloud"></span><span id="CLOUD"></span>**雲**
</dt> <dd>

實際的雲端價值。

</dd> <dt>

<span id="enCloudState"></span><span id="encloudstate"></span><span id="ENCLOUDSTATE"></span>**enCloudState**
</dt> <dd>

雲端的目前狀態。 [**PNRP \_雲端 \_ 狀態**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_cloud_state) 會指定有效的值。

</dd> <dt>

<span id="enCloudFlags"></span><span id="encloudflags"></span><span id="ENCLOUDFLAGS"></span>**enCloudFlags**
</dt> <dd>

指出雲端名稱在網路上有效，或僅適用于目前的電腦。 [**PNRP \_雲端 \_ 旗標**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_cloud_flags) 會指定有效的值。 某些雲端名稱在相同網路上的任何電腦上都是有效的。 其他雲端名稱只有在目前的電腦上才有效，而且可能只會在一段時間內有效。

-   如果 **enCloudFlags** 設定為 **PNRP \_ 雲端 \_ 名稱 \_ LOCAL，** 則名稱只在本機有效。
-   如果未設定 **enCloudFlags** ，則雲端名稱可以轉移到其他電腦。

</dd> </dl>

## <a name="related-topics"></a>相關主題

<dl> <dt>

[PNRP 和 BLOB](pnrp-and-blob.md)
</dt> <dt>

[PNRP 和 WSALookupServiceEnd](pnrp-and-wsalookupserviceend.md)
</dt> <dt>

[PNRP 和 WSANSPIoctl](pnrp-and-wsanspioctl.md)
</dt> <dt>

[PNRP 和 WSAQUERYSET](pnrp-and-wsaqueryset.md)
</dt> <dt>

[**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo)
</dt> <dt>

[**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)
</dt> <dt>

[PNRP NSP 錯誤碼](pnrp-nsp-error-codes.md)
</dt> <dt>

[**WSALookupServiceBegin**](winsock-nsp-reference-links.md)
</dt> </dl>

 

 



