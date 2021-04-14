---
title: ITsSbTarget IpAddresses 屬性
description: 捕獲或指定目標的外部 IP 位址。
ms.assetid: 938a753c-d541-4772-b41b-817324488685
ms.tgt_platform: multiple
keywords:
- TargetExternalIpAddresses 屬性遠端桌面服務
- TargetExternalIpAddresses 屬性遠端桌面服務，ITsSbTarget 介面
- TargetExternalIpAddresses 屬性遠端桌面服務，ITsSbTarget 介面
- IpAddresses 屬性遠端桌面服務
- IpAddresses 屬性遠端桌面服務，ITsSbTarget 介面
- ITsSbTarget 介面遠端桌面服務，IpAddresses 屬性
- IpAddresses 屬性遠端桌面服務，ITsSbTargetEx 介面
- ITsSbTargetEx 介面遠端桌面服務，IpAddresses 屬性
topic_type:
- apiref
api_name:
- ITsSbTarget.IpAddresses
- ITsSbTarget.get_IpAddresses
- ITsSbTarget.put_IpAddresses
- ITsSbTargetEx.IpAddresses
- ITsSbTargetEx.get_IpAddresses
- ITsSbTargetEx.put_IpAddresses
- TargetExternalIpAddresses
- ITsSbTarget.TargetExternalIpAddresses
- ITsSbTarget get_TargetExternalIpAddresses
- ITsSbTarget put_TargetExternalIpAddresses
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8b3902840b24bc49ae3bda0510c8355afb67810
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104373006"
---
# <a name="itssbtargetipaddresses-property"></a>ITsSbTarget：： IpAddresses 屬性

捕獲或指定目標的外部 IP 位址。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_IpAddresses(
  [in, size_is(numAddresses)]   TSSD_ConnectionPoint *sockaddr,
  [in]                          DWORD                numAddresses
);

HRESULT get_IpAddresses(
  [out, size_is(*numAddresses)] TSSD_ConnectionPoint *sockaddr,
  [in, out]                     DWORD                *numAddresses
);
```



## <a name="property-value"></a>屬性值

[**TSSD \_ ConnectionPoint**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint)結構陣列的指標，此陣列會接收目標的外部 IP 位址。

**DWORD** 變數的指標，其中包含 *sockaddr* 參數中的外部 IP 位址數目。 如果位址數目不明，請將 *sockaddr* 傳遞為 **Null**。 方法會傳回在 *sockaddr* 參數所指向的陣列中配置所需的 [**TSSD \_ ConnectionPoint**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint)結構數目。

## <a name="remarks"></a>備註

此屬性在 Windows Server 2008 R2 中先前稱為 **TargetExternalIpAddresses** 。

如果外部 IP 位址的數目未知，您可以呼叫這個方法，並將 *sockaddr* 設定為 **Null**。 方法接著會在 *numAddresses* 參數中傳回接收所有外部 IP 位址所需的 [**TSSD \_ ConnectionPoint**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint) 結構數目。 根據此數位配置 *sockaddr* 的陣列，然後再次呼叫方法，將 *sockaddr* 設定為新配置的陣列，並 *numAddresses* 至第一個呼叫傳回的數位。

## <a name="requirements"></a>規格需求



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>最低支援的用戶端<br/></td>
<td>都不支援<br/></td>
</tr>
<tr class="even">
<td>最低支援的伺服器<br/></td>
<td>Windows Server 2012<br/></td>
</tr>
<tr class="odd">
<td>Idl<br/></td>
<td><dl> <dt>Sbtsv .idl</dt> </dl></td>
</tr>
<tr class="even">
<td>IID<br/></td>
<td>IID_ITsSbTarget 定義為：
<ul>
<li>16616ECC-272D-411D-B324-126893033856</li>
<li>e85e10ea-db0b-4752-b456-5fd5840901c0 on Windows Server 2008 R2</li>
</ul></td>
</tr>
</tbody>
</table>



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITsSbTargetEx**](itssbtargetex.md)
</dt> <dt>

[**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> <dt>

[**TSSD \_ ConnectionPoint**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint)
</dt> </dl>

 

 





