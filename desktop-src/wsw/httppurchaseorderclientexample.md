---
title: HttpPurchaseOrderClientExample
description: 此範例示範如何使用服務 proxy 來與 HTTP 型 PurchaseOrder 服務通訊。
ms.assetid: e577b06c-28b1-4f8f-a6af-025b9672cf27
keywords:
- HttpPurchaseOrderClientExample 原生 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fa6a883fa6c9ec041bb1454ba7074c06bd20c61
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021638"
---
# <a name="httppurchaseorderclientexample"></a><span data-ttu-id="1f9ae-106">HttpPurchaseOrderClientExample</span><span class="sxs-lookup"><span data-stu-id="1f9ae-106">HttpPurchaseOrderClientExample</span></span>

<span data-ttu-id="1f9ae-107">此範例示範如何使用服務 proxy 來與 HTTP 型 PurchaseOrder 服務通訊。</span><span class="sxs-lookup"><span data-stu-id="1f9ae-107">This example show how to use the service proxy to talk to an HTTP based PurchaseOrder service.</span></span>

-   [<span data-ttu-id="1f9ae-108">HttpPurchaseOrderClient .cpp</span><span class="sxs-lookup"><span data-stu-id="1f9ae-108">HttpPurchaseOrderClient.cpp</span></span>](#httppurchaseorderclientcpp)
-   [<span data-ttu-id="1f9ae-109">PurchaseOrder .wsdl</span><span class="sxs-lookup"><span data-stu-id="1f9ae-109">PurchaseOrder.wsdl</span></span>](#purchaseorderwsdl)
-   [<span data-ttu-id="1f9ae-110">Makefile</span><span class="sxs-lookup"><span data-stu-id="1f9ae-110">Makefile</span></span>](#makefile)

## <a name="httppurchaseorderclientcpp"></a><span data-ttu-id="1f9ae-111">HttpPurchaseOrderClient .cpp</span><span class="sxs-lookup"><span data-stu-id="1f9ae-111">HttpPurchaseOrderClient.cpp</span></span>


```C++
//------------------------------------------------------------
// Copyright (C) Microsoft.  All rights reserved.
//------------------------------------------------------------

#ifndef UNICODE
#define UNICODE
#endif
#include <windows.h>
#include <stdio.h>
#include "WebServices.h"
#include "process.h"
#include "string.h"
#include "PurchaseOrder.wsdl.h"

// Print out rich error info
void PrintError(HRESULT errorCode, WS_ERROR* error)
{
    wprintf(L"Failure: errorCode=0x%lx\n", errorCode);

    if (errorCode == E_INVALIDARG || errorCode == WS_E_INVALID_OPERATION)
    {
        // Correct use of the APIs should never generate these errors
        wprintf(L"The error was due to an invalid use of an API.  This is likely due to a bug in the program.\n");
        DebugBreak();
    }

    HRESULT hr = NOERROR;
    if (error != NULL)
    {
        ULONG errorCount;
        hr = WsGetErrorProperty(error, WS_ERROR_PROPERTY_STRING_COUNT, &errorCount, sizeof(errorCount));
        if (FAILED(hr))
        {
            goto Exit;
        }
        for (ULONG i = 0; i < errorCount; i++)
        {
            WS_STRING string;
            hr = WsGetErrorString(error, i, &string);
            if (FAILED(hr))
            {
                goto Exit;
            }
            wprintf(L"%.*s\n", string.length, string.chars);
        }
    }
Exit:
    if (FAILED(hr))
    {
        wprintf(L"Could not get error string (errorCode=0x%lx)\n", hr);
    }
}
// Main entry point
int __cdecl wmain(int argc, __in_ecount(argc) wchar_t **argv)
{
    UNREFERENCED_PARAMETER(argc);
    UNREFERENCED_PARAMETER(argv);
    
    HRESULT hr = NOERROR;
    WS_ERROR* error = NULL;
    WS_HEAP* heap = NULL;
    WS_SERVICE_PROXY* serviceProxy = NULL;
    WS_STRING serviceUrl = WS_STRING_VALUE(L"http://localhost/example");
    
    
    WS_STRING productName;
    WS_STRING expectedShipDate;
    WS_STRING orderStatus;
    WS_ENDPOINT_ADDRESS address = {};
    address.url = serviceUrl;
    
    
    // Create an error object for storing rich error information
    hr = WsCreateError(
        NULL, 
        0, 
        &error);
    if (FAILED(hr))
    {
        goto Exit;
    }
    // Create a heap to store deserialized data
    hr = WsCreateHeap(
        /*maxSize*/ 2048, 
        /*trimSize*/ 512, 
        NULL, 
        0, 
        &heap, 
        error);
    if (FAILED(hr))
    {
        goto Exit;
    }
    hr = WsCreateServiceProxy(
        WS_CHANNEL_TYPE_REQUEST, 
        WS_HTTP_CHANNEL_BINDING, 
        NULL, 
        NULL, 
        0, 
        NULL, 
        0, 
        &serviceProxy, 
        error);
    if (FAILED(hr))
    {
        goto Exit;
    }
    
    
    hr = WsOpenServiceProxy(
        serviceProxy, 
        &address, 
        NULL, 
        error);
    if (FAILED(hr))
    {
        goto Exit;
    }
    productName.chars = L"Pencil";
    productName.length = 6;
    
    for (int i = 0; i < 100; i++)
    {
        unsigned int orderID;
    
        // Submit an order, and get expected ship date
        hr = PurchaseOrderBinding_Order(
            serviceProxy, 
            100, 
            productName, 
            &orderID, 
            &expectedShipDate, 
            heap, 
            NULL, 
            0, 
            NULL, 
            error);
    
        if (FAILED(hr))
        {
            goto Exit;
        }
    
        // Print out confirmation contents
        wprintf(L"Expected ship date for order %lu is %.*s\n",
            orderID,
            expectedShipDate.length,
            expectedShipDate.chars);
        
        WsResetHeap(heap, NULL);
        
        // Get the current status of the order
        hr = PurchaseOrderBinding_OrderStatus(
            serviceProxy, 
            &orderID, 
            &orderStatus, 
            heap, 
            NULL, 
            0, 
            NULL, 
            error);
    
        if (FAILED(hr))
        {
            goto Exit;
        }
    
        // Print out order status
        wprintf(L"Order status for order %lu is: %.*s\n",
            orderID,
            orderStatus.length,
            orderStatus.chars);
        
        WsResetHeap(
            heap, 
            NULL);
    
        // Get the current status of the order using an invalid order ID
        orderID = 321;
        hr = PurchaseOrderBinding_OrderStatus(
            serviceProxy, 
            &orderID, 
            &orderStatus, 
            heap, 
            NULL, 
            0, 
            NULL, 
            error);
    
        // Check to see if we got a fault
        if (hr == WS_E_ENDPOINT_FAULT_RECEIVED)
        {
            // Print the strings in the error object
            PrintError(hr, error);
        
            // TODO: the following should be removed when wsutil generates it
            WS_XML_STRING _faultDetailName = WS_XML_STRING_VALUE("OrderNotFound");
            WS_XML_STRING _faultDetailNs = WS_XML_STRING_VALUE("http://example.com");
            WS_XML_STRING _faultAction = WS_XML_STRING_VALUE("http://example.com/fault");
            WS_ELEMENT_DESCRIPTION _faultElementDescription = { &_faultDetailName, &_faultDetailNs, WS_UINT32_TYPE, NULL };
            WS_FAULT_DETAIL_DESCRIPTION orderNotFoundFaultTypeDescription = { &_faultAction, &_faultElementDescription };
        
            // Try to get the fault detail from the error object
            _OrderNotFoundFaultType* orderNotFound;
            hr = WsGetFaultErrorDetail(
                error,
                &orderNotFoundFaultTypeDescription,
                WS_READ_OPTIONAL_POINTER,
                heap,
                &orderNotFound,
                sizeof(orderNotFound));
                
            if (FAILED(hr))
            {
                goto Exit;
            }
        
            if (orderNotFound != NULL)
            {
                // Print out the fault detail
                wprintf(L"Order %lu was not found\n", orderNotFound->orderID);
            }
        
            // Reset error so it can be used again
            hr = WsResetError(error);
            if (FAILED(hr))
            {
                goto Exit;
            }
        }
    
        if (FAILED(hr))
        {
            goto Exit;
        }
    
        WsResetHeap(heap, NULL);
    
        wprintf(L"\n");
    }
                   
Exit:
    if (FAILED(hr))
    {
        // Print out the error
        PrintError(hr, error);
    }
    fflush(
        stdout);
    if (serviceProxy != NULL)
    {
        WsCloseServiceProxy(serviceProxy, NULL, NULL);
        WsFreeServiceProxy(serviceProxy);
    }
    
    
    if (heap != NULL)
    {
        WsFreeHeap(heap);
    }
    if (error != NULL)
    {
        WsFreeError(error);
    }
    fflush(stdout);
    return SUCCEEDED(hr) ? 0 : -1;
}


```



## <a name="purchaseorderwsdl"></a><span data-ttu-id="1f9ae-112">PurchaseOrder .wsdl</span><span class="sxs-lookup"><span data-stu-id="1f9ae-112">PurchaseOrder.wsdl</span></span>

``` syntax
<wsdl:definitions 
    xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" 
    xmlns:tns="http://example.org" 
    xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
    xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" 
    xmlns:soap12="http://schemas.xmlsoap.org/wsdl/soap12/" 
    xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/" 
    targetNamespace="http://example.org">
    <wsdl:types>
        <xsd:schema targetNamespace="http://example.org" elementFormDefault="qualified">
            <xsd:element name="PurchaseOrderType">
                <xsd:complexType>
                    <xsd:sequence>
                        <xsd:element minOccurs="0" name="quantity" type="xsd:int"/>
                        <xsd:element minOccurs="0" name="productName" type="xsd:string"/>
                    </xsd:sequence>
                </xsd:complexType>
            </xsd:element>
            <xsd:element name="OrderConfirmationType">
                <xsd:complexType>
                    <xsd:sequence>
                        <xsd:element minOccurs="0" name="orderID" type="xsd:unsignedInt"/>
                        <xsd:element minOccurs="0" name="expectedShipDate" type="xsd:string"/>
                    </xsd:sequence>
                </xsd:complexType>
            </xsd:element>
            <xsd:element name="GetOrderStatusType">
                <xsd:complexType>
                    <xsd:sequence>
                        <xsd:element minOccurs="0" name="orderID" type="xsd:unsignedInt"/>
                    </xsd:sequence>
                </xsd:complexType>
            </xsd:element>
            <xsd:element name="GetOrderStatusResponseType">
                <xsd:complexType>
                    <xsd:sequence>
                        <xsd:element minOccurs="0" name="orderID" type="xsd:unsignedInt"/>
                        <xsd:element minOccurs="0" name="status" type="xsd:string"/>
                    </xsd:sequence>
                </xsd:complexType>
            </xsd:element>
            <xsd:element name="OrderNotFoundFaultType">
                <xsd:complexType>
                    <xsd:sequence>
                        <xsd:element minOccurs="0" name="orderID" type="xsd:unsignedInt"/>
                    </xsd:sequence>
                </xsd:complexType>
            </xsd:element>
        </xsd:schema>
    </wsdl:types>
    <wsdl:message name="PurchaseOrder">
        <wsdl:part name="parameters" element="tns:PurchaseOrderType"/>
    </wsdl:message>
    <wsdl:message name="OrderConfirmation">
        <wsdl:part name="parameters" element="tns:OrderConfirmationType"/>
    </wsdl:message>
    <wsdl:message name="GetOrderStatus">
        <wsdl:part name="parameters" element="tns:GetOrderStatusType"/>
    </wsdl:message>
    <wsdl:message name="GetOrderStatusResponse">
        <wsdl:part name="parameters" element="tns:GetOrderStatusResponseType"/>
    </wsdl:message>
    <wsdl:message name="OrderNotFoundFault">
        <wsdl:part name="parameters" element="tns:OrderNotFoundFaultType"/>
    </wsdl:message>
    <wsdl:portType name="IPurchaseOrder">
        <wsdl:operation name="Order">
            <wsdl:input message="tns:PurchaseOrder" wsaw:Action="http://example.org/purchaseorder"/>
            <wsdl:output message="tns:OrderConfirmation" wsaw:Action="http://example.org/orderconfirmation"/>
        </wsdl:operation>
        <wsdl:operation name="OrderStatus">
            <wsdl:input message="tns:GetOrderStatus" wsaw:Action="http://example.org/getorderstatus"/>
            <wsdl:output message="tns:GetOrderStatusResponse" wsaw:Action="http://example.org/getorderstatusresponse"/>
            <wsdl:fault name="OrderNotFound" message="tns:OrderNotFoundFault" wsaw:Action="http://example.org/ordernotfound"/>
        </wsdl:operation>
    </wsdl:portType>
    <wsdl:binding name="PurchaseOrderBinding" type="tns:IPurchaseOrder">
        <soap:binding transport="http://schemas.xmlsoap.org/soap/http"/>
        <wsdl:operation name="Order">
            <soap:operation soapAction="http://example.org/purchaseorder" style="document"/>
            <wsdl:input>
                <soap:body use="literal"/>
            </wsdl:input>
            <wsdl:output>
                <soap:body use="literal"/>
            </wsdl:output>
        </wsdl:operation>
        <wsdl:operation name="OrderStatus">
            <soap:operation soapAction="http://example.org/getorderstatus" style="document"/>
            <wsdl:input>
                <soap:body use="literal"/>
            </wsdl:input>
            <wsdl:output>
                <soap:body use="literal"/>
            </wsdl:output>
            <wsdl:fault name="OrderNotFound">
                <soap:body use="literal"/>
            </wsdl:fault>
        </wsdl:operation>
    </wsdl:binding>
    <wsdl:service name="PurchaseOrderService">
        <wsdl:port name="IPurchaseOrder" binding="tns:PurchaseOrderBinding">
            <soap:address location="http://example.org/IPurchaseOrder"/>
        </wsdl:port>
    </wsdl:service>
</wsdl:definitions>
```

## <a name="makefile"></a><span data-ttu-id="1f9ae-113">Makefile</span><span class="sxs-lookup"><span data-stu-id="1f9ae-113">Makefile</span></span>

``` syntax
!include <Win32.Mak>

EXTRA_LIBS = WebServices.lib rpcrt4.lib Iphlpapi.lib

all: $(OUTDIR) $(OUTDIR)\WsHttpPurchaseOrderClient.exe

"$(OUTDIR)" :
    if not exist "$(OUTDIR)/$(NULL)" mkdir "$(OUTDIR)"
    
$(OUTDIR)\PurchaseOrder.wsdl.c: PurchaseOrder.wsdl
     Wsutil.exe /wsdl:PurchaseOrder.wsdl /string:WS_STRING /out:$(OUTDIR)
    
$(OUTDIR)\PurchaseOrder.wsdl.obj: $(OUTDIR)\PurchaseOrder.wsdl.c
    $(cc) $(cdebug) $(cflags) $(cvarsmt) /WX -I$(OUTDIR) /Fo"$(OUTDIR)\\" /Fd"$(OUTDIR)\\" $(OUTDIR)\PurchaseOrder.wsdl.c

$(OUTDIR)\HttpPurchaseOrderClient.obj: HttpPurchaseOrderClient.cpp $(OUTDIR)\PurchaseOrder.wsdl.c
    $(cc) $(cdebug) $(cflags) $(cvarsmt) /WX -I$(OUTDIR) /Fo"$(OUTDIR)\\" /Fd"$(OUTDIR)\\" HttpPurchaseOrderClient.cpp

$(OUTDIR)\WsHttpPurchaseOrderClient.exe: $(OUTDIR)\HttpPurchaseOrderClient.obj $(OUTDIR)\PurchaseOrder.wsdl.obj
    $(link) $(ldebug) $(conlflags) $(conlibsmt) $(EXTRA_LIBS) -out:$(OUTDIR)\WsHttpPurchaseOrderClient.exe $(OUTDIR)\HttpPurchaseOrderClient.obj $(OUTDIR)\PurchaseOrder.wsdl.obj /PDB:$(OUTDIR)\WsHttpPurchaseOrderClient.PDB

clean:
    $(CLEANUP)
```

 

 




