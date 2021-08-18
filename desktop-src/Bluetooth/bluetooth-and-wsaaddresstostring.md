---
title: 藍牙和 WSAAddressToString
description: WSAAddressToString Windows 通訊端函式可用來將藍牙的裝置位址轉換成字串，然後在抓取裝置服務資訊時，透過 WSAQUERYSET 結構提供給 WSALookupServiceBegin 函數。
ms.assetid: 3489d29a-2b64-4051-b579-57878efc0c73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65bb49563355b3a85ff64d7168f77e8526ca1679cffaa565e7b9cd7070cf87f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004278"
---
# <a name="bluetooth-and-wsaaddresstostring"></a>藍牙和 WSAAddressToString

[**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) Windows 通訊端函式可用來將藍牙的裝置位址轉換成字串，然後在抓取裝置服務資訊時，透過 [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)結構提供給 [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)函數。

雖然藍牙的裝置位址符合20個字元的緩衝區，但 [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa)函式目前會針對藍牙裝置位址傳回 **WSAEFAULT** ，除非緩衝區和指定的 *lpdwAddressStringLength* 值設定為40的字元長度。

> [!Note]  
> 當 [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa)由於緩衝區不足而傳回 **WSAEFAULT** 時，不會使用作業所需的緩衝區大小來更新 *lpdwAddressStringLength* 參數。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa)
</dt> <dt>

[藍牙和 WSALookupServiceBegin](bluetooth-and-wsalookupservicebegin.md)
</dt> <dt>

[藍牙和 WSAQUERYSET](bluetooth-and-wsaqueryset.md)
</dt> </dl>

 

 