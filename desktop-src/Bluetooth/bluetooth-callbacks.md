---
title: 藍牙回呼
description: 本節中的藍牙回呼函式會與能夠管理藍牙裝置和服務的函式搭配使用。
ms.assetid: a66f88e2-46f7-4e23-9b61-7ee35abec207
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1afe99dc3fe1bee8f133cddae0e319e6354077e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671608"
---
# <a name="bluetooth-callbacks"></a><span data-ttu-id="62924-103">藍牙回呼</span><span class="sxs-lookup"><span data-stu-id="62924-103">Bluetooth Callbacks</span></span>

<span data-ttu-id="62924-104">本節中的藍牙回呼函式會與能夠管理藍牙裝置和服務的函式搭配使用。</span><span class="sxs-lookup"><span data-stu-id="62924-104">The Bluetooth callback functions in this section are used in combination with functions that make it possible to manage Bluetooth devices and services.</span></span>

<span data-ttu-id="62924-105">您也可以使用 Windows 通訊端程式設計介面來支援藍牙。</span><span class="sxs-lookup"><span data-stu-id="62924-105">Bluetooth is also supported by using the Windows Sockets programming interface.</span></span> <span data-ttu-id="62924-106">如需使用 Windows 通訊端介面進行藍牙程式設計的詳細資訊，請參閱 [適用于藍牙的 Windows 通訊端支援](windows-sockets-support-for-bluetooth.md)。</span><span class="sxs-lookup"><span data-stu-id="62924-106">For more information about programming Bluetooth by using the Windows Sockets interface, see [Windows Sockets Support for Bluetooth](windows-sockets-support-for-bluetooth.md).</span></span>



| <span data-ttu-id="62924-107">區段</span><span class="sxs-lookup"><span data-stu-id="62924-107">Section</span></span>                                                                                      | <span data-ttu-id="62924-108">Content</span><span class="sxs-lookup"><span data-stu-id="62924-108">Content</span></span>                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="62924-109">**PFN \_ AUTHENTICATION \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="62924-109">**PFN\_AUTHENTICATION\_CALLBACK**</span></span>](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_authentication_callback)                         | <span data-ttu-id="62924-110">搭配 [**BluetoothRegisterForAuthentication**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication) 函式使用。</span><span class="sxs-lookup"><span data-stu-id="62924-110">Used in conjunction with the [**BluetoothRegisterForAuthentication**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication) function.</span></span>                                                  |
| [<span data-ttu-id="62924-111">**PFN \_ AUTHENTICATION \_ 回呼， \_ 例如**</span><span class="sxs-lookup"><span data-stu-id="62924-111">**PFN\_AUTHENTICATION\_CALLBACK\_EX**</span></span>](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_authentication_callback_ex)                  | <span data-ttu-id="62924-112">搭配 [**BluetoothRegisterForAuthenticationEx**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthenticationex) 函式使用。</span><span class="sxs-lookup"><span data-stu-id="62924-112">Used in conjunction with the [**BluetoothRegisterForAuthenticationEx**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthenticationex) function.</span></span>                                              |
| [<span data-ttu-id="62924-113">**PFN \_ 藍牙 \_ 列舉 \_ 屬性 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="62924-113">**PFN\_BLUETOOTH\_ENUM\_ATTRIBUTES\_CALLBACK**</span></span>](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_bluetooth_enum_attributes_callback) | <span data-ttu-id="62924-114">針對在傳遞至 [**BluetoothSdpEnumAttributes**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpenumattributes)函式呼叫的 *pSDPStream* 參數中找到的每個屬性呼叫一次。</span><span class="sxs-lookup"><span data-stu-id="62924-114">Called once for each attribute found in the *pSDPStream* parameter that is passed to the [**BluetoothSdpEnumAttributes**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpenumattributes) function call.</span></span> |
| [<span data-ttu-id="62924-115">**PFN \_ 裝置 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="62924-115">**PFN\_DEVICE\_CALLBACK**</span></span>](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_device_callback)                                         | <span data-ttu-id="62924-116">用於與選取藍牙裝置的關聯。</span><span class="sxs-lookup"><span data-stu-id="62924-116">Used in association with selecting Bluetooth devices.</span></span>                                                                                                                    |



 

 

 




